---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/powershell/module/az.analysisservices/set-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Set-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Set-AzAnalysisServicesServer.md
ms.openlocfilehash: b39da37f41e3a18bc70f25fe36d67301e49867c9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959306"
---
# <span data-ttu-id="4aaf5-101">Set-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="4aaf5-101">Set-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="4aaf5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4aaf5-102">SYNOPSIS</span></span>
<span data-ttu-id="4aaf5-103">Modyfikuje wystąpienie serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="4aaf5-103">Modifies  an instance of Analysis Services server</span></span>

## <span data-ttu-id="4aaf5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4aaf5-104">SYNTAX</span></span>

### <span data-ttu-id="4aaf5-105">Domyślne (domyślne)</span><span class="sxs-lookup"><span data-stu-id="4aaf5-105">Default (Default)</span></span>
```
Set-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>] [-PassThru]
 [-ReadonlyReplicaCount <Int32>] [-DefaultConnectionMode <String>]
 [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>] [-GatewayResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4aaf5-106">DisableBackup</span><span class="sxs-lookup"><span data-stu-id="4aaf5-106">DisableBackup</span></span>
```
Set-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-DisableBackup] [-ReadonlyReplicaCount <Int32>]
 [-DefaultConnectionMode <String>] [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4aaf5-107">DisassociateGateway</span><span class="sxs-lookup"><span data-stu-id="4aaf5-107">DisassociateGateway</span></span>
```
Set-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-ReadonlyReplicaCount <Int32>]
 [-DefaultConnectionMode <String>] [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>]
 [-DisassociateGateway] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4aaf5-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="4aaf5-108">DESCRIPTION</span></span>
<span data-ttu-id="4aaf5-109">Polecenie Set-AzAnalysisServicesServer modyfikuje wystąpienie serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="4aaf5-109">The Set-AzAnalysisServicesServer cmdlet modifies an instance of Analysis Services server</span></span>

## <span data-ttu-id="4aaf5-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4aaf5-110">EXAMPLES</span></span>

### <span data-ttu-id="4aaf5-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4aaf5-111">Example 1</span></span>
```
PS C:\> Set-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup" -Tag "key1:value1,key2:value2" -Administrator "testuser1@contoso.com"
```

<span data-ttu-id="4aaf5-112">Modyfikuje serwer o nazwie serwer testowy w grupie testowej grupy zasobów, aby ustawić tagi jako klucz1:wartość1 i wartość2:wartość2, a administrator do testuser1@contoso.com</span><span class="sxs-lookup"><span data-stu-id="4aaf5-112">Modifies the server named testserver in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com</span></span>

## <span data-ttu-id="4aaf5-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4aaf5-113">PARAMETERS</span></span>

### <span data-ttu-id="4aaf5-114">— Administrator</span><span class="sxs-lookup"><span data-stu-id="4aaf5-114">-Administrator</span></span>
<span data-ttu-id="4aaf5-115">Ciąg reprezentujący rozdzieloną przecinkami listę użytkowników lub grup, które mają zostać ustawione jako administratorzy na serwerze.</span><span class="sxs-lookup"><span data-stu-id="4aaf5-115">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span>
<span data-ttu-id="4aaf5-116">Użytkownikom lub grupom należy określić format UPN, user@contoso.com np. groups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="4aaf5-116">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

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

### <span data-ttu-id="4aaf5-117">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="4aaf5-117">-BackupBlobContainerUri</span></span>
<span data-ttu-id="4aaf5-118">Uri kontenera obiektów blob do tworzenia kopii zapasowej serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="4aaf5-118">The blob container Uri for backup the Analysis Services server</span></span>

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

### <span data-ttu-id="4aaf5-119">-DefaultConnectionMode</span><span class="sxs-lookup"><span data-stu-id="4aaf5-119">-DefaultConnectionMode</span></span>
<span data-ttu-id="4aaf5-120">Domyślny tryb połączenia serwera usługi Analysis</span><span class="sxs-lookup"><span data-stu-id="4aaf5-120">Default connection mode of an Analysis service server</span></span>

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

### <span data-ttu-id="4aaf5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4aaf5-121">-DefaultProfile</span></span>
<span data-ttu-id="4aaf5-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4aaf5-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4aaf5-123">-DisableBackup</span><span class="sxs-lookup"><span data-stu-id="4aaf5-123">-DisableBackup</span></span>
<span data-ttu-id="4aaf5-124">Przełącznik, aby wyłączyć zapasowy kontener obiektów blob.</span><span class="sxs-lookup"><span data-stu-id="4aaf5-124">The switch to disable backup blob container.</span></span>
<span data-ttu-id="4aaf5-125">Aby ponownie włączyć zapasowy kontener obiektów blob, podaj zapasowy kontener obiektów blob Uri jako -BackupBlobContainerUri.</span><span class="sxs-lookup"><span data-stu-id="4aaf5-125">To re-enable the backup blob container, please provide the backup blob container Uri as -BackupBlobContainerUri.</span></span>

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

### <span data-ttu-id="4aaf5-126">-DisasssociateGateway</span><span class="sxs-lookup"><span data-stu-id="4aaf5-126">-DisassociateGateway</span></span>
<span data-ttu-id="4aaf5-127">Disasssociate Gateway resource from an Analysis server</span><span class="sxs-lookup"><span data-stu-id="4aaf5-127">Disassociate Gateway resource from an Analysis server</span></span>

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

### <span data-ttu-id="4aaf5-128">- FirewallConfig</span><span class="sxs-lookup"><span data-stu-id="4aaf5-128">-FirewallConfig</span></span>
<span data-ttu-id="4aaf5-129">Konfiguracja zapory serwera analysis</span><span class="sxs-lookup"><span data-stu-id="4aaf5-129">Firewall config of an Analysis server</span></span>

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

### <span data-ttu-id="4aaf5-130">-GatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="4aaf5-130">-GatewayResourceId</span></span>
<span data-ttu-id="4aaf5-131">Identyfikator zasobu bramy do skojarzenia z serwerem analizy</span><span class="sxs-lookup"><span data-stu-id="4aaf5-131">Gateway resource Id to associate to an Analysis server</span></span>

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

### <span data-ttu-id="4aaf5-132">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4aaf5-132">-Name</span></span>
<span data-ttu-id="4aaf5-133">Nazwa serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="4aaf5-133">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="4aaf5-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4aaf5-134">-PassThru</span></span>
<span data-ttu-id="4aaf5-135">Jeśli operacja zostanie pomyślnie ukończona, zostaną zwrócone szczegóły usuniętego serwera.</span><span class="sxs-lookup"><span data-stu-id="4aaf5-135">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="4aaf5-136">-ReadonlyReplicaCount</span><span class="sxs-lookup"><span data-stu-id="4aaf5-136">-ReadonlyReplicaCount</span></span>
<span data-ttu-id="4aaf5-137">Tylko do odczytu liczba replik serwera usługi Analysis</span><span class="sxs-lookup"><span data-stu-id="4aaf5-137">Read only replica count of an Analysis service server</span></span>

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

### <span data-ttu-id="4aaf5-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4aaf5-138">-ResourceGroupName</span></span>
<span data-ttu-id="4aaf5-139">Nazwa grupy zasobów platformy Azure, do której należy serwer</span><span class="sxs-lookup"><span data-stu-id="4aaf5-139">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="4aaf5-140">- SKU</span><span class="sxs-lookup"><span data-stu-id="4aaf5-140">-Sku</span></span>
<span data-ttu-id="4aaf5-141">Nazwa sku dla serwera.</span><span class="sxs-lookup"><span data-stu-id="4aaf5-141">The name of the Sku for the server.</span></span>
<span data-ttu-id="4aaf5-142">Obsługiwane wartości to S0, 'S1', 'S2', 'S4', 'S8', 'S9', 'S8v2', 'S9v2' dla warstwy standardowej; "B1", "B2" dla warstwy podstawowej i "D1" dla warstwy rozwoju.</span><span class="sxs-lookup"><span data-stu-id="4aaf5-142">The supported values are 'S0', 'S1', 'S2', 'S4', 'S8', 'S9', 'S8v2', 'S9v2' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

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

### <span data-ttu-id="4aaf5-143">— Tag</span><span class="sxs-lookup"><span data-stu-id="4aaf5-143">-Tag</span></span>
<span data-ttu-id="4aaf5-144">Pary klucz-wartość w postaci tabeli skrótów ustawionej jako tagi na serwerze.</span><span class="sxs-lookup"><span data-stu-id="4aaf5-144">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

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

### <span data-ttu-id="4aaf5-145">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4aaf5-145">-Confirm</span></span>
<span data-ttu-id="4aaf5-146">Monituje użytkownika o potwierdzenie, czy wykonać operację</span><span class="sxs-lookup"><span data-stu-id="4aaf5-146">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="4aaf5-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4aaf5-147">-WhatIf</span></span>
<span data-ttu-id="4aaf5-148">W tym artykule opisano akcje, które bieżąca operacja zostanie wykonać bez ich wykonania.</span><span class="sxs-lookup"><span data-stu-id="4aaf5-148">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="4aaf5-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4aaf5-149">CommonParameters</span></span>
<span data-ttu-id="4aaf5-150">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4aaf5-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4aaf5-151">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4aaf5-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4aaf5-152">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4aaf5-152">INPUTS</span></span>

### <span data-ttu-id="4aaf5-153">System.String</span><span class="sxs-lookup"><span data-stu-id="4aaf5-153">System.String</span></span>

### <span data-ttu-id="4aaf5-154">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="4aaf5-154">System.Collections.Hashtable</span></span>

### <span data-ttu-id="4aaf5-155">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="4aaf5-155">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="4aaf5-156">System.Int32</span><span class="sxs-lookup"><span data-stu-id="4aaf5-156">System.Int32</span></span>

### <span data-ttu-id="4aaf5-157">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="4aaf5-157">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="4aaf5-158">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4aaf5-158">OUTPUTS</span></span>

### <span data-ttu-id="4aaf5-159">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="4aaf5-159">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="4aaf5-160">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4aaf5-160">NOTES</span></span>
<span data-ttu-id="4aaf5-161">Alias: Set-AzAs</span><span class="sxs-lookup"><span data-stu-id="4aaf5-161">Alias: Set-AzAs</span></span>

## <span data-ttu-id="4aaf5-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4aaf5-162">RELATED LINKS</span></span>

[<span data-ttu-id="4aaf5-163">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="4aaf5-163">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="4aaf5-164">Remove-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="4aaf5-164">Remove-AzAnalysisServicesServer</span></span>](./Remove-AzAnalysisServicesServer.md)
