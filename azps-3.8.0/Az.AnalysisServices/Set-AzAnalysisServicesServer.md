---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/set-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Set-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Set-AzAnalysisServicesServer.md
ms.openlocfilehash: d13ffe73ada97ba68825beeb1769572767b3561a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050931"
---
# <span data-ttu-id="febb7-101">Set-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="febb7-101">Set-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="febb7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="febb7-102">SYNOPSIS</span></span>
<span data-ttu-id="febb7-103">Modyfikowanie wystąpienia serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="febb7-103">Modifies  an instance of Analysis Services server</span></span>

## <span data-ttu-id="febb7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="febb7-104">SYNTAX</span></span>

### <span data-ttu-id="febb7-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="febb7-105">Default (Default)</span></span>
```
Set-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>] [-PassThru]
 [-ReadonlyReplicaCount <Int32>] [-DefaultConnectionMode <String>]
 [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>] [-GatewayResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="febb7-106">DisableBackup</span><span class="sxs-lookup"><span data-stu-id="febb7-106">DisableBackup</span></span>
```
Set-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-DisableBackup] [-ReadonlyReplicaCount <Int32>]
 [-DefaultConnectionMode <String>] [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="febb7-107">DisassociateGateway</span><span class="sxs-lookup"><span data-stu-id="febb7-107">DisassociateGateway</span></span>
```
Set-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-ReadonlyReplicaCount <Int32>]
 [-DefaultConnectionMode <String>] [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>]
 [-DisassociateGateway] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="febb7-108">Opis</span><span class="sxs-lookup"><span data-stu-id="febb7-108">DESCRIPTION</span></span>
<span data-ttu-id="febb7-109">Polecenie cmdlet Set-AzAnalysisServicesServer modyfikuje wystąpienie serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="febb7-109">The Set-AzAnalysisServicesServer cmdlet modifies an instance of Analysis Services server</span></span>

## <span data-ttu-id="febb7-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="febb7-110">EXAMPLES</span></span>

### <span data-ttu-id="febb7-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="febb7-111">Example 1</span></span>
```
PS C:\> Set-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup" -Tag "key1:value1,key2:value2" -Administrator "testuser1@contoso.com"
```

<span data-ttu-id="febb7-112">Modyfikuje serwer o nazwie TestServer w zbiorze testerów zasobów, aby ustawić Tagi jako KEY1: wartość1 i key2: wartość2 i administrator, aby testuser1@contoso.com</span><span class="sxs-lookup"><span data-stu-id="febb7-112">Modifies the server named testserver in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com</span></span>

## <span data-ttu-id="febb7-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="febb7-113">PARAMETERS</span></span>

### <span data-ttu-id="febb7-114">-Administrator</span><span class="sxs-lookup"><span data-stu-id="febb7-114">-Administrator</span></span>
<span data-ttu-id="febb7-115">Ciąg reprezentujący rozdzielaną przecinkami listę użytkowników lub grup, które mają być ustawiane jako Administratorzy na serwerze.</span><span class="sxs-lookup"><span data-stu-id="febb7-115">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span>
<span data-ttu-id="febb7-116">Użytkownicy lub grupy muszą być określeni jako format UPN, np. user@contoso.comgroups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="febb7-116">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="febb7-117">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="febb7-117">-BackupBlobContainerUri</span></span>
<span data-ttu-id="febb7-118">Identyfikator URI kontenera obiektu BLOB na potrzeby tworzenia kopii zapasowych serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="febb7-118">The blob container Uri for backup the Analysis Services server</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="febb7-119">-DefaultConnectionMode</span><span class="sxs-lookup"><span data-stu-id="febb7-119">-DefaultConnectionMode</span></span>
<span data-ttu-id="febb7-120">Domyślny tryb połączenia serwera usługi Analysis Services</span><span class="sxs-lookup"><span data-stu-id="febb7-120">Default connection mode of an Analysis service server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: All, Readonly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="febb7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="febb7-121">-DefaultProfile</span></span>
<span data-ttu-id="febb7-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="febb7-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="febb7-123">-DisableBackup</span><span class="sxs-lookup"><span data-stu-id="febb7-123">-DisableBackup</span></span>
<span data-ttu-id="febb7-124">Przełącznik umożliwiający wyłączenie kontenera obiektu BLOB kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="febb7-124">The switch to disable backup blob container.</span></span>
<span data-ttu-id="febb7-125">Aby ponownie włączyć kontener obiektu BLOB kopii zapasowej, podaj identyfikator URI kontenera obiektów BLOB kopii zapasowej w postaci-BackupBlobContainerUri.</span><span class="sxs-lookup"><span data-stu-id="febb7-125">To re-enable the backup blob container, please provide the backup blob container Uri as -BackupBlobContainerUri.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableBackup
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="febb7-126">-DisassociateGateway</span><span class="sxs-lookup"><span data-stu-id="febb7-126">-DisassociateGateway</span></span>
<span data-ttu-id="febb7-127">Usuwanie skojarzenia zasobu bramy z serwera analiz</span><span class="sxs-lookup"><span data-stu-id="febb7-127">Disassociate Gateway resource from an Analysis server</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisassociateGateway
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="febb7-128">-FirewallConfig</span><span class="sxs-lookup"><span data-stu-id="febb7-128">-FirewallConfig</span></span>
<span data-ttu-id="febb7-129">Konfiguracja zapory serwera analiz</span><span class="sxs-lookup"><span data-stu-id="febb7-129">Firewall config of an Analysis server</span></span>

```yaml
Type: Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="febb7-130">-GatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="febb7-130">-GatewayResourceId</span></span>
<span data-ttu-id="febb7-131">Identyfikator zasobu bramy skojarzony z serwerem analizy</span><span class="sxs-lookup"><span data-stu-id="febb7-131">Gateway resource Id to associate to an Analysis server</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="febb7-132">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="febb7-132">-Name</span></span>
<span data-ttu-id="febb7-133">Nazwa serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="febb7-133">Name of the Analysis Services server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="febb7-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="febb7-134">-PassThru</span></span>
<span data-ttu-id="febb7-135">Po pomyślnym zakończeniu operacji zwróci dane usuniętego serwera.</span><span class="sxs-lookup"><span data-stu-id="febb7-135">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="febb7-136">-ReadonlyReplicaCount</span><span class="sxs-lookup"><span data-stu-id="febb7-136">-ReadonlyReplicaCount</span></span>
<span data-ttu-id="febb7-137">Liczba replik tylko do odczytu serwera usługi Analysis Services</span><span class="sxs-lookup"><span data-stu-id="febb7-137">Read only replica count of an Analysis service server</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="febb7-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="febb7-138">-ResourceGroupName</span></span>
<span data-ttu-id="febb7-139">Nazwa grupy zasobów platformy Azure, do której należy serwer</span><span class="sxs-lookup"><span data-stu-id="febb7-139">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="febb7-140">-SKU</span><span class="sxs-lookup"><span data-stu-id="febb7-140">-Sku</span></span>
<span data-ttu-id="febb7-141">Nazwa jednostki SKU serwera.</span><span class="sxs-lookup"><span data-stu-id="febb7-141">The name of the Sku for the server.</span></span>
<span data-ttu-id="febb7-142">Obsługiwane wartości to 0 ', 1 ', 2 ', 4 ' dla warstwy standardowej; "B1"; "B2" dla warstwy podstawowej i 1 "dla warstwy rozwoju.</span><span class="sxs-lookup"><span data-stu-id="febb7-142">The supported values are 'S0', 'S1', 'S2', 'S4' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="febb7-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="febb7-143">-Tag</span></span>
<span data-ttu-id="febb7-144">Pary klucz-wartość w formie tabeli skrótów ustawione jako znaczniki na serwerze.</span><span class="sxs-lookup"><span data-stu-id="febb7-144">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="febb7-145">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="febb7-145">-Confirm</span></span>
<span data-ttu-id="febb7-146">Monituje użytkownika o potwierdzenie, czy wykonać operację.</span><span class="sxs-lookup"><span data-stu-id="febb7-146">Prompts user to confirm whether to perform the operation</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="febb7-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="febb7-147">-WhatIf</span></span>
<span data-ttu-id="febb7-148">Opisuje akcje, które zostaną wykonane przez bieżącą operację bez ich rzeczywistego wykonywania.</span><span class="sxs-lookup"><span data-stu-id="febb7-148">Describes the actions the current operation will perform without actually performing them</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="febb7-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="febb7-149">CommonParameters</span></span>
<span data-ttu-id="febb7-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="febb7-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="febb7-151">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="febb7-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="febb7-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="febb7-152">INPUTS</span></span>

### <span data-ttu-id="febb7-153">System. String</span><span class="sxs-lookup"><span data-stu-id="febb7-153">System.String</span></span>

### <span data-ttu-id="febb7-154">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="febb7-154">System.Collections.Hashtable</span></span>

### <span data-ttu-id="febb7-155">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="febb7-155">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="febb7-156">System. Int32</span><span class="sxs-lookup"><span data-stu-id="febb7-156">System.Int32</span></span>

### <span data-ttu-id="febb7-157">Microsoft. Azure. Commands. AnalysisServices. models. PsAzureAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="febb7-157">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="febb7-158">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="febb7-158">OUTPUTS</span></span>

### <span data-ttu-id="febb7-159">Microsoft. Azure. Commands. AnalysisServices. models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="febb7-159">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="febb7-160">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="febb7-160">NOTES</span></span>
<span data-ttu-id="febb7-161">Alias: Set-AzAs</span><span class="sxs-lookup"><span data-stu-id="febb7-161">Alias: Set-AzAs</span></span>

## <span data-ttu-id="febb7-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="febb7-162">RELATED LINKS</span></span>

[<span data-ttu-id="febb7-163">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="febb7-163">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="febb7-164">Remove-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="febb7-164">Remove-AzAnalysisServicesServer</span></span>](./Remove-AzAnalysisServicesServer.md)
