---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/set-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Set-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Set-AzAnalysisServicesServer.md
ms.openlocfilehash: a3c3338db7fb749b3eb4d5e92c438deda0742a67
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063745"
---
# <span data-ttu-id="2b739-101">Set-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="2b739-101">Set-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="2b739-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2b739-102">SYNOPSIS</span></span>
<span data-ttu-id="2b739-103">Modyfikowanie wystąpienia serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="2b739-103">Modifies  an instance of Analysis Services server</span></span>

## <span data-ttu-id="2b739-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2b739-104">SYNTAX</span></span>

### <span data-ttu-id="2b739-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="2b739-105">Default (Default)</span></span>
```
Set-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>] [-PassThru]
 [-ReadonlyReplicaCount <Int32>] [-DefaultConnectionMode <String>]
 [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>] [-GatewayResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b739-106">DisableBackup</span><span class="sxs-lookup"><span data-stu-id="2b739-106">DisableBackup</span></span>
```
Set-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-DisableBackup] [-ReadonlyReplicaCount <Int32>]
 [-DefaultConnectionMode <String>] [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b739-107">DisassociateGateway</span><span class="sxs-lookup"><span data-stu-id="2b739-107">DisassociateGateway</span></span>
```
Set-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-ReadonlyReplicaCount <Int32>]
 [-DefaultConnectionMode <String>] [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>]
 [-DisassociateGateway] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b739-108">Opis</span><span class="sxs-lookup"><span data-stu-id="2b739-108">DESCRIPTION</span></span>
<span data-ttu-id="2b739-109">Polecenie cmdlet Set-AzAnalysisServicesServer modyfikuje wystąpienie serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="2b739-109">The Set-AzAnalysisServicesServer cmdlet modifies an instance of Analysis Services server</span></span>

## <span data-ttu-id="2b739-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2b739-110">EXAMPLES</span></span>

### <span data-ttu-id="2b739-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2b739-111">Example 1</span></span>
```
PS C:\> Set-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup" -Tag "key1:value1,key2:value2" -Administrator "testuser1@contoso.com"
```

<span data-ttu-id="2b739-112">Modyfikuje serwer o nazwie TestServer w zbiorze testerów zasobów, aby ustawić Tagi jako KEY1: wartość1 i key2: wartość2 i administrator, aby testuser1@contoso.com</span><span class="sxs-lookup"><span data-stu-id="2b739-112">Modifies the server named testserver in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com</span></span>

## <span data-ttu-id="2b739-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2b739-113">PARAMETERS</span></span>

### <span data-ttu-id="2b739-114">-Administrator</span><span class="sxs-lookup"><span data-stu-id="2b739-114">-Administrator</span></span>
<span data-ttu-id="2b739-115">Ciąg reprezentujący rozdzielaną przecinkami listę użytkowników lub grup, które mają być ustawiane jako Administratorzy na serwerze.</span><span class="sxs-lookup"><span data-stu-id="2b739-115">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span>
<span data-ttu-id="2b739-116">Użytkownicy lub grupy muszą być określeni jako format UPN, np. user@contoso.comgroups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="2b739-116">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

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

### <span data-ttu-id="2b739-117">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="2b739-117">-BackupBlobContainerUri</span></span>
<span data-ttu-id="2b739-118">Identyfikator URI kontenera obiektu BLOB na potrzeby tworzenia kopii zapasowych serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="2b739-118">The blob container Uri for backup the Analysis Services server</span></span>

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

### <span data-ttu-id="2b739-119">-DefaultConnectionMode</span><span class="sxs-lookup"><span data-stu-id="2b739-119">-DefaultConnectionMode</span></span>
<span data-ttu-id="2b739-120">Domyślny tryb połączenia serwera usługi Analysis Services</span><span class="sxs-lookup"><span data-stu-id="2b739-120">Default connection mode of an Analysis service server</span></span>

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

### <span data-ttu-id="2b739-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b739-121">-DefaultProfile</span></span>
<span data-ttu-id="2b739-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2b739-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b739-123">-DisableBackup</span><span class="sxs-lookup"><span data-stu-id="2b739-123">-DisableBackup</span></span>
<span data-ttu-id="2b739-124">Przełącznik umożliwiający wyłączenie kontenera obiektu BLOB kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="2b739-124">The switch to disable backup blob container.</span></span>
<span data-ttu-id="2b739-125">Aby ponownie włączyć kontener obiektu BLOB kopii zapasowej, podaj identyfikator URI kontenera obiektów BLOB kopii zapasowej w postaci-BackupBlobContainerUri.</span><span class="sxs-lookup"><span data-stu-id="2b739-125">To re-enable the backup blob container, please provide the backup blob container Uri as -BackupBlobContainerUri.</span></span>

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

### <span data-ttu-id="2b739-126">-DisassociateGateway</span><span class="sxs-lookup"><span data-stu-id="2b739-126">-DisassociateGateway</span></span>
<span data-ttu-id="2b739-127">Usuwanie skojarzenia zasobu bramy z serwera analiz</span><span class="sxs-lookup"><span data-stu-id="2b739-127">Disassociate Gateway resource from an Analysis server</span></span>

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

### <span data-ttu-id="2b739-128">-FirewallConfig</span><span class="sxs-lookup"><span data-stu-id="2b739-128">-FirewallConfig</span></span>
<span data-ttu-id="2b739-129">Konfiguracja zapory serwera analiz</span><span class="sxs-lookup"><span data-stu-id="2b739-129">Firewall config of an Analysis server</span></span>

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

### <span data-ttu-id="2b739-130">-GatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="2b739-130">-GatewayResourceId</span></span>
<span data-ttu-id="2b739-131">Identyfikator zasobu bramy skojarzony z serwerem analizy</span><span class="sxs-lookup"><span data-stu-id="2b739-131">Gateway resource Id to associate to an Analysis server</span></span>

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

### <span data-ttu-id="2b739-132">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2b739-132">-Name</span></span>
<span data-ttu-id="2b739-133">Nazwa serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="2b739-133">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="2b739-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2b739-134">-PassThru</span></span>
<span data-ttu-id="2b739-135">Po pomyślnym zakończeniu operacji zwróci dane usuniętego serwera.</span><span class="sxs-lookup"><span data-stu-id="2b739-135">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="2b739-136">-ReadonlyReplicaCount</span><span class="sxs-lookup"><span data-stu-id="2b739-136">-ReadonlyReplicaCount</span></span>
<span data-ttu-id="2b739-137">Liczba replik tylko do odczytu serwera usługi Analysis Services</span><span class="sxs-lookup"><span data-stu-id="2b739-137">Read only replica count of an Analysis service server</span></span>

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

### <span data-ttu-id="2b739-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b739-138">-ResourceGroupName</span></span>
<span data-ttu-id="2b739-139">Nazwa grupy zasobów platformy Azure, do której należy serwer</span><span class="sxs-lookup"><span data-stu-id="2b739-139">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="2b739-140">-SKU</span><span class="sxs-lookup"><span data-stu-id="2b739-140">-Sku</span></span>
<span data-ttu-id="2b739-141">Nazwa jednostki SKU serwera.</span><span class="sxs-lookup"><span data-stu-id="2b739-141">The name of the Sku for the server.</span></span>
<span data-ttu-id="2b739-142">Obsługiwane są wartości z zakresu od 0 do 1 ', 2 ', 4 ', ', ', ', ' 8v2 ', ', 9v2 ' dla standardowej warstwy; "B1"; "B2" dla warstwy podstawowej i 1 "dla warstwy rozwoju.</span><span class="sxs-lookup"><span data-stu-id="2b739-142">The supported values are 'S0', 'S1', 'S2', 'S4', 'S8', 'S9', 'S8v2', 'S9v2' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

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

### <span data-ttu-id="2b739-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="2b739-143">-Tag</span></span>
<span data-ttu-id="2b739-144">Pary klucz-wartość w formie tabeli skrótów ustawione jako znaczniki na serwerze.</span><span class="sxs-lookup"><span data-stu-id="2b739-144">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

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

### <span data-ttu-id="2b739-145">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2b739-145">-Confirm</span></span>
<span data-ttu-id="2b739-146">Monituje użytkownika o potwierdzenie, czy wykonać operację.</span><span class="sxs-lookup"><span data-stu-id="2b739-146">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="2b739-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b739-147">-WhatIf</span></span>
<span data-ttu-id="2b739-148">Opisuje akcje, które zostaną wykonane przez bieżącą operację bez ich rzeczywistego wykonywania.</span><span class="sxs-lookup"><span data-stu-id="2b739-148">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="2b739-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b739-149">CommonParameters</span></span>
<span data-ttu-id="2b739-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b739-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b739-151">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b739-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b739-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2b739-152">INPUTS</span></span>

### <span data-ttu-id="2b739-153">System. String</span><span class="sxs-lookup"><span data-stu-id="2b739-153">System.String</span></span>

### <span data-ttu-id="2b739-154">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2b739-154">System.Collections.Hashtable</span></span>

### <span data-ttu-id="2b739-155">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2b739-155">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="2b739-156">System. Int32</span><span class="sxs-lookup"><span data-stu-id="2b739-156">System.Int32</span></span>

### <span data-ttu-id="2b739-157">Microsoft. Azure. Commands. AnalysisServices. models. PsAzureAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="2b739-157">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="2b739-158">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2b739-158">OUTPUTS</span></span>

### <span data-ttu-id="2b739-159">Microsoft. Azure. Commands. AnalysisServices. models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="2b739-159">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="2b739-160">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2b739-160">NOTES</span></span>
<span data-ttu-id="2b739-161">Alias: Set-AzAs</span><span class="sxs-lookup"><span data-stu-id="2b739-161">Alias: Set-AzAs</span></span>

## <span data-ttu-id="2b739-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2b739-162">RELATED LINKS</span></span>

[<span data-ttu-id="2b739-163">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="2b739-163">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="2b739-164">Remove-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="2b739-164">Remove-AzAnalysisServicesServer</span></span>](./Remove-AzAnalysisServicesServer.md)
