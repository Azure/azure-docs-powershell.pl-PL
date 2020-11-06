---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 1A2C843C-6962-4B0E-ACBF-A5EFF609A5BE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVmss.md
ms.openlocfilehash: 9f6135917f2e6cbfc05511637b3b20bd126d54b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524550"
---
# New-AzureRmVmss

## STRESZCZENIe
Tworzy VMSS.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### DefaultParameter (domyślny)
```
New-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SimpleParameterSet
```
New-AzureRmVmss [[-ResourceGroupName] <String>] [-VMScaleSetName] <String> [-AsJob] [-ImageName <String>]
 -Credential <PSCredential> [-InstanceCount <Int32>] [-VirtualNetworkName <String>] [-SubnetName <String>]
 [-PublicIpAddressName <String>] [-DomainNameLabel <String>] [-SecurityGroupName <String>]
 [-LoadBalancerName <String>] [-BackendPort <Int32[]>] [-Location <String>] [-VmSize <String>]
 [-UpgradePolicyMode <UpgradeMode>] [-AllocationMethod <String>] [-VnetAddressPrefix <String>]
 [-SubnetAddressPrefix <String>] [-FrontendPoolName <String>] [-BackendPoolName <String>]
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-NatBackendPort <Int32[]>]
 [-DataDiskSizeInGb <Int32[]>] [-DefaultProfile <IAzureContextContainer>] [-SinglePlacementGroup] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzureRmVmss** umożliwia utworzenie zestawu skali maszyny wirtualnej (VMSS) na platformie Azure.
Użyj prostego zestawu parametrów ( `SimpleParameterSet` ), aby szybko utworzyć wstępnie ustawiony VMSS i skojarzone zasoby. Użyj domyślnego zestawu parametrów ( `DefaultParameter` ), aby bardziej zaawansowane scenariusze można było precyzyjnie skonfigurować poszczególne składniki VMSS oraz wszystkie skojarzone z nimi zasoby przed utworzeniem.

## Przykłady

### Przykład 1. Tworzenie VMSS przy użyciu **`SimpleParameterSet`**
```powershell
$vmssName = <VMSSNAME>
# Create credentials, I am using one way to create credentials, there are others as well. 
# Pick one that makes the most sense according to your use case.
$vmPassword = ConvertTo-SecureString <PASSWORD_HERE> -AsPlainText -Force
$vmCred = New-Object System.Management.Automation.PSCredential(<USERNAME_HERE>, $vmPassword)

#Create a VMSS using the default settings
New-AzureRmVmss -Credential $vmCred -VMScaleSetName $vmssName
```

W powyższym poleceniu zostanie utworzona następująca nazwa `$vmssName` :
* Grupa zasobów
* Sieć wirtualna
* Moduł równoważenia obciążenia
* Publiczny adres IP
* VMSS z dwoma wystąpieniami

Domyślnym obrazem wybranym dla maszyn wirtualnych w VMSS jest `2016-Datacenter Windows Server` , a wersja SKU to `Standard_DS1_v2`

### Przykład 2: Tworzenie VMSS przy użyciu **`DefaultParameterSet`**
```powershell
# Common
$LOC = "WestUs";
$RGName = "rgkyvms";

New-AzureRmResourceGroup -Name $RGName -Location $LOC -Force;

# SRP
$STOName = "STO" + $RGName;
$STOType = "Standard_GRS";
New-AzureRmStorageAccount -ResourceGroupName $RGName -Name $STOName -Location $LOC -Type $STOType;
$STOAccount = Get-AzureRmStorageAccount -ResourceGroupName $RGName -Name $STOName; 

# NRP
$SubNet = New-AzureRmVirtualNetworkSubnetConfig -Name ("subnet" + $RGName) -AddressPrefix "10.0.0.0/24";
$VNet = New-AzureRmVirtualNetwork -Force -Name ("vnet" + $RGName) -ResourceGroupName $RGName -Location $LOC -AddressPrefix "10.0.0.0/16" -DnsServer "10.1.1.1" -Subnet $SubNet;
$VNet = Get-AzureRmVirtualNetwork -Name ('vnet' + $RGName) -ResourceGroupName $RGName;
$SubNetId = $VNet.Subnets[0].Id;

$PubIP = New-AzureRmPublicIpAddress -Force -Name ("PubIP" + $RGName) -ResourceGroupName $RGName -Location $LOC -AllocationMethod Dynamic -DomainNameLabel ("PubIP" + $RGName);
$PubIP = Get-AzureRmPublicIpAddress -Name ("PubIP"  + $RGName) -ResourceGroupName $RGName;

# Create LoadBalancer
$FrontendName = "fe" + $RGName
$BackendAddressPoolName = "bepool" + $RGName
$ProbeName = "vmssprobe" + $RGName
$InboundNatPoolName  = "innatpool" + $RGName
$LBRuleName = "lbrule" + $RGName
$LBName = "vmsslb" + $RGName

$Frontend = New-AzureRmLoadBalancerFrontendIpConfig -Name $FrontendName -PublicIpAddress $PubIP
$BackendAddressPool = New-AzureRmLoadBalancerBackendAddressPoolConfig -Name $BackendAddressPoolName
$Probe = New-AzureRmLoadBalancerProbeConfig -Name $ProbeName -RequestPath healthcheck.aspx -Protocol http -Port 80 -IntervalInSeconds 15 -ProbeCount 2
$InboundNatPool = New-AzureRmLoadBalancerInboundNatPoolConfig -Name $InboundNatPoolName  -FrontendIPConfigurationId `
    $Frontend.Id -Protocol Tcp -FrontendPortRangeStart 3360 -FrontendPortRangeEnd 3362 -BackendPort 3370;
$LBRule = New-AzureRmLoadBalancerRuleConfig -Name $LBRuleName `
    -FrontendIPConfiguration $Frontend -BackendAddressPool $BackendAddressPool `
    -Probe $Probe -Protocol Tcp -FrontendPort 80 -BackendPort 80 `
    -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP;
$ActualLb = New-AzureRmLoadBalancer -Name $LBName -ResourceGroupName $RGName -Location $LOC `
    -FrontendIpConfiguration $Frontend -BackendAddressPool $BackendAddressPool `
    -Probe $Probe -LoadBalancingRule $LBRule -InboundNatPool $InboundNatPool;
$ExpectedLb = Get-AzureRmLoadBalancer -Name $LBName -ResourceGroupName $RGName

# New VMSS Parameters
$VMSSName = "VMSS" + $RGName;

$AdminUsername = "Admin01";
$AdminPassword = "p4ssw0rd@123" + $RGName;

$PublisherName = "MicrosoftWindowsServer" 
$Offer         = "WindowsServer" 
$Sku           = "2012-R2-Datacenter" 
$Version       = "latest"
        
$VHDContainer = "https://" + $STOName + ".blob.core.contoso.net/" + $VMSSName;

$ExtName = "CSETest";
$Publisher = "Microsoft.Compute";
$ExtType = "BGInfo";
$ExtVer = "2.1";

#IP Config for the NIC
$IPCfg = New-AzureRmVmssIPConfig -Name "Test" `
    -LoadBalancerInboundNatPoolsId $ExpectedLb.InboundNatPools[0].Id `
    -LoadBalancerBackendAddressPoolsId $ExpectedLb.BackendAddressPools[0].Id `
    -SubnetId $SubNetId;
            
#VMSS Config
$VMSS = New-AzureRmVmssConfig -Location $LOC -SkuCapacity 2 -SkuName "Standard_A2" -UpgradePolicyMode "Automatic" `
    | Add-AzureRmVmssNetworkInterfaceConfiguration -Name "Test" -Primary $True -IPConfiguration $IPCfg `
    | Add-AzureRmVmssNetworkInterfaceConfiguration -Name "Test2"  -IPConfiguration $IPCfg `
    | Set-AzureRmVmssOSProfile -ComputerNamePrefix "Test"  -AdminUsername $AdminUsername -AdminPassword $AdminPassword `
    | Set-AzureRmVmssStorageProfile -Name "Test"  -OsDiskCreateOption 'FromImage' -OsDiskCaching "None" `
    -ImageReferenceOffer $Offer -ImageReferenceSku $Sku -ImageReferenceVersion $Version `
    -ImageReferencePublisher $PublisherName -VhdContainer $VHDContainer `
    | Add-AzureRmVmssExtension -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True

#Create the VMSS
New-AzureRmVmss -ResourceGroupName $RGName -Name $VMSSName -VirtualMachineScaleSet $VMSS;
```

W złożonym przykładzie powyżej powstaje VMSS, poniżej przedstawiono wyjaśnienie, co się dzieje:
* Pierwsze polecenie tworzy grupę zasobów o określonej nazwie i lokalizacji.
* Drugie polecenie używa polecenia cmdlet **New-AzureRmStorageAccount** w celu utworzenia konta magazynu.
* Trzecia komenda używa polecenia cmdlet **Get-AzureRmStorageAccount** w celu uzyskania konta magazynu utworzonego w drugim poleceniu i zapisanie wyniku w zmiennej $STOAccount.
* W piątym poleceniu użyto polecenia cmdlet **New-AzureRmVirtualNetworkSubnetConfig** w celu utworzenia podsieci i zapisanie wyniku w zmiennej o nazwie $Subnet.
* W szóstym poleceniu użyto polecenia cmdlet **New-AzureRmVirtualNetwork** w celu utworzenia sieci wirtualnej i zapisu wyniku w zmiennej o nazwie $VNET.
* W przypadku siódmego polecenia w celu uzyskania informacji o sieci wirtualnej utworzonej w szóstym poleceniu jest używane polecenie **Get-AzureRmVirtualNetwork** , a informacje są przechowywane w zmiennej o nazwie $VNET.
* W przypadku ośmiu i Dziewiątych poleceń do tworzenia i pobierania informacji z tego publicznego adresu IP użyto polecenia **New-AzureRmPublicIpAddress** i **Get-AzureRmPublicIpAddress** .
* Te polecenia przechowują informacje w zmiennej o nazwie $PubIP.
* W poleceniu dziesiątym użyto polecenia cmdlet **New-AzureRmLoadBalancerFrontendIpConfig** w celu utworzenia modułu równoważenia obciążenia frontonu i zapisu wyniku w zmiennej o nazwie $frontend.
* W jedenastym poleceniu użyto polecenia **New-AzureRmLoadBalancerBackendAddressPoolConfig** w celu utworzenia konfiguracji puli adresów zaplecza i zapisu wyniku w zmiennej o nazwie $BackendAddressPool.
* W poleceniu dwunasta jest używana funkcja **New-AzureRmLoadBalancerProbeConfig** w celu utworzenia sondy i zapisanie informacji dotyczących sondy w zmiennej o nazwie $Probe.
* Polecenie trzynaste używa polecenia cmdlet **New-AzureRmLoadBalancerInboundNatPoolConfig** w celu utworzenia konfiguracji puli NAT (Network Address Translation) modułu równoważenia obciążenia.
* Polecenie czternaste używa polecenia **New-AzureRmLoadBalancerRuleConfig** w celu utworzenia konfiguracji reguł modułu równoważenia obciążenia i zapisu wyniku w zmiennej o nazwie $LBRule.
* W poleceniu piętnaste polecenie cmdlet **New-AzureRmLoadBalancer** jest używane do utworzenia modułu równoważenia obciążenia i zapisuje wynik w zmiennej o nazwie $ActualLb.
* Polecenie szesnaste używa polecenia **Get-AzureRmLoadBalancer** w celu uzyskania informacji na temat modułu równoważenia obciążenia utworzonego w piętnastym poleceniu i zapisanie informacji w zmiennej o nazwie $ExpectedLb.
* W poleceniu siedemnasta użyto polecenia cmdlet **New-AzureRmVmssIPConfig** w celu utworzenia VMSS konfiguracji adresu IP i zapisu informacji w zmiennej o nazwie $IPCfg.
* Polecenie osiemnastym miesiącem korzysta z polecenia cmdlet **New-AzureRmVmssConfig** w celu utworzenia obiektu konfiguracji VMSS i zapisanie wyniku w zmiennej o nazwie $VMSS.
* W poleceniu XIX użyto polecenia cmdlet **New-AzureRmVmss** w celu utworzenia VMSS.

## PARAMETRÓW

### -AllocationMethod
Metoda alokacji dla publicznego adresu IP zestawu skali (statycznego lub dynamicznego).  Jeśli nie podano żadnej wartości, alokacja będzie statyczna.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:
Accepted values: Static, Dynamic

Required: False
Position: Named
Default value: Static
Accept pipeline input: False
Accept wildcard characters: False
```

### -AsJob
Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackendPoolName
Nazwa puli adresów zaplecza, która ma być używana w usłudze równoważenia obciążenia dla tego zestawu skali.  Jeśli nie podano żadnej wartości, zostanie utworzona nowa pula zaplecza z tą samą nazwą co zestaw skali.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackendPort
Numery portów zaplecza używane przez moduł skalowania, ustawiony w celu komunikowania się z maszynami wirtualnymi w zestawie skali.  Jeśli nie określono żadnych wartości, porty 3389 i 5985 będą używane na potrzeby maszyn wirtualnych systemu Windows, a w przypadku maszyn wirtualnych Linux będzie używana wartość port 22.

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Poświadczenie
Poświadczenia administratora (nazwa użytkownika i hasło) dla maszyn wirtualnych w tym zestawie skali.

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: SimpleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DataDiskSizeInGb
Określa rozmiary dysków z danymi w GB.

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainNameLabel
Etykieta nazwy domeny dla publicznej nazwy domeny Fully-Qualified (FQDN) dla tego zestawu skali. Jest to pierwszy składnik nazwy domeny, który jest automatycznie przypisywany do zestawu skali. Automatycznie przypisane nazwy domen używają formularza ( <DomainNameLabel> . <Location> . cloudapp.azure.com). Jeśli nie zostanie podana żadna wartość, domyślna etykieta nazwy domeny będzie łączyć się z <ScaleSetName> i <ResourceGroupName> .

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FrontendPoolName
Nazwa puli adresów frontonu, która ma być używana w usłudze równoważenia obciążenia ustawionej na poziomie skali.  Jeśli nie podano żadnej wartości, zostanie utworzona nowa pula adresów frontonu o takiej samej nazwie jak ustawiona skala.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ImageName
Nazwa obrazu maszyny wirtualnej w tym zestawie skali. Jeśli nie podano żadnej wartości, zostanie wykorzystany obraz "Windows Server 2016 DataCenter".

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstanceCount
Liczba obrazów maszyny wirtualnej w zestawie skali.  Jeśli nie podano żadnej wartości, zostaną utworzone 2 wystąpienia.

```yaml
Type: System.Int32
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: 2
Accept pipeline input: False
Accept wildcard characters: False
```

### -LoadBalancerName
Nazwa modułu równoważenia obciążenia do użycia z tym zestawem skali.  Jeśli nie zostanie określona żadna wartość, zostanie utworzona nowa usługa równoważenia obciążenia z tą samą nazwą co zestaw skali.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Lokalizacja
Lokalizacja platformy Azure, w której zostanie utworzony ten zestaw skali.  Jeśli nie podano żadnej wartości, lokalizacja zostanie wywnioskowana z lokalizacji innych zasobów, do których odwołuje się parametr.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NatBackendPort
Port zaplecza translacji adresów sieciowych.

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicIpAddressName
Nazwa publicznego adresu IP, który ma być używany z tym zestawem skali.  Jeśli nie zostanie podana żadna wartość, zostanie utworzony nowy publiczny adres IP o takiej samej nazwie jak zestaw skali.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów VMSS.  Jeśli nie podano żadnej wartości, zostanie utworzony nowy element resourceName o tej samej nazwie co zestaw skali.

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SecurityGroupName
Nazwa grupy zabezpieczeń sieci do zastosowania do tego zestawu skali.  Jeśli nie podano żadnej wartości, zostanie utworzona i zastosowana domyślna grupa zabezpieczeń sieci z tą samą nazwą co zestaw skali.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SinglePlacementGroup
Za pomocą tej pozycji można utworzyć zestaw skali w jednej grupie położenia, domyślnie jest to wiele grup

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetAddressPrefix
Prefiks adresu podsieci, który będzie używany przez tę ScaleSet. Domyślne ustawienia podsieci (192.168.1.0/24) zostaną zastosowane, jeśli nie podano żadnej wartości.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.1.0/24
Accept pipeline input: False
Accept wildcard characters: False
```

### -Subnetname
Nazwa podsieci do użycia z tym zestawem skali.  Zostanie utworzona nowa podsieć o takiej samej nazwie jak skala ustawiona, jeśli nie podano żadnej wartości.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SystemAssignedIdentity
Jeśli parametr jest obecny, w przypadku maszyn wirtualnych w zestawie skali jest przypisana automatycznie generowana tożsamość systemu zarządzanego.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UpgradePolicyMode
Tryb zasad uaktualniania dla wystąpień maszyny wirtualnej w tym zestawie skali.  Zasady uaktualniania mogą określać uaktualnianie automatyczne, ręczne lub stopniowe.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.UpgradeMode
Parameter Sets: SimpleParameterSet
Aliases:
Accepted values: Automatic, Manual, Rolling

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserAssignedIdentity
Nazwa tożsamości usługi zarządzanej, która powinna być przypisana do maszyn wirtualnych w zestawie skali.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualMachineScaleSet
Określa obiekt **VirtualMachineScaleSet** , który zawiera właściwości VMSS, które tworzy polecenie cmdlet.

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VirtualNetworkName
Nazwa fo sieci wirtualnej do użycia z tym zestawem skali.  Jeśli nie podano żadnej wartości, zostanie utworzona nowa sieć wirtualna o takiej samej nazwie jak zestaw skali.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VMScaleSetName
Określa nazwę VMSS, które tworzy polecenie cmdlet.

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VmSize
Rozmiar wystąpień maszyny wirtualnej w tym zestawie skali.  Jeśli nie określono rozmiaru, zostanie wykorzystana wartość domyślna (Standard_DS1_v2).

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: Standard_DS1_v2
Accept pipeline input: False
Accept wildcard characters: False
```

### -VnetAddressPrefix
Prefiks adresu sieci wirtualnej używanej z tym zestawem skali.  Jeśli nie zostanie podana żadna wartość, zostanie użyty domyślny prefiks adresu sieci wirtualnej (192.168.0.0/16).

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.0.0/16
Accept pipeline input: False
Accept wildcard characters: False
```

### -Zone
Lista stref dostępności oznaczająca adres IP przydzielony dla zasobu musi pochodzić od.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Potwierdź
Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.
Polecenie cmdlet nie jest uruchamiane.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. String

### Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet
Parametry: VirtualMachineScaleSet (ByValue)

### System. Collections. Generic. list "1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]

## WYSYŁA

### Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureRmVmss](./Get-AzureRmVmss.md)

[Remove-AzureRmVmss](./Remove-AzureRmVmss.md)

[Restart-AzureRmVmss](./Restart-AzureRmVmss.md)

[Set-AzureRmVmss](./Set-AzureRmVmss.md)

[Start — AzureRmVmss](./Start-AzureRmVmss.md)

[Zatrzymaj — AzureRmVmss](./Stop-AzureRmVmss.md)

[Update-AzureRmVmss](./Update-AzureRmVmss.md)


