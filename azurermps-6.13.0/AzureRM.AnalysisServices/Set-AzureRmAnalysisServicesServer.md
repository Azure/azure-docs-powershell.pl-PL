---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/set-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Set-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Set-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 30f5e7237f497f3d9f4208548b56ede72583f067
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717986"
---
# <span data-ttu-id="3c40e-101">Set-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="3c40e-101">Set-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="3c40e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3c40e-102">SYNOPSIS</span></span>
<span data-ttu-id="3c40e-103">Modyfikowanie wystąpienia serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="3c40e-103">Modifies  an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c40e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3c40e-104">SYNTAX</span></span>

### <span data-ttu-id="3c40e-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="3c40e-105">Default (Default)</span></span>
```
Set-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>] [-PassThru]
 [-ReadonlyReplicaCount <Int32>] [-DefaultConnectionMode <String>]
 [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>] [-GatewayResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c40e-106">DisableBackup</span><span class="sxs-lookup"><span data-stu-id="3c40e-106">DisableBackup</span></span>
```
Set-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-DisableBackup] [-ReadonlyReplicaCount <Int32>]
 [-DefaultConnectionMode <String>] [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c40e-107">DisassociateGateway</span><span class="sxs-lookup"><span data-stu-id="3c40e-107">DisassociateGateway</span></span>
```
Set-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-ReadonlyReplicaCount <Int32>]
 [-DefaultConnectionMode <String>] [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>]
 [-DisassociateGateway] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c40e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="3c40e-108">DESCRIPTION</span></span>
<span data-ttu-id="3c40e-109">Polecenie cmdlet Set-AzureRmAnalysisServicesServer modyfikuje wystąpienie serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="3c40e-109">The Set-AzureRmAnalysisServicesServer cmdlet modifies an instance of Analysis Services server</span></span>

## <span data-ttu-id="3c40e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3c40e-110">EXAMPLES</span></span>

### <span data-ttu-id="3c40e-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3c40e-111">Example 1</span></span>
```
PS C:\> Set-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup" -Tag "key1:value1,key2:value2" -Administrator "testuser1@contoso.com"
```

<span data-ttu-id="3c40e-112">Modyfikuje serwer o nazwie TestServer w zbiorze testerów zasobów, aby ustawić Tagi jako KEY1: wartość1 i key2: wartość2 i administrator, aby testuser1@contoso.com</span><span class="sxs-lookup"><span data-stu-id="3c40e-112">Modifies the server named testserver in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com</span></span>

## <span data-ttu-id="3c40e-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3c40e-113">PARAMETERS</span></span>

### <span data-ttu-id="3c40e-114">-Administrator</span><span class="sxs-lookup"><span data-stu-id="3c40e-114">-Administrator</span></span>
<span data-ttu-id="3c40e-115">Ciąg reprezentujący rozdzielaną przecinkami listę użytkowników lub grup, które mają być ustawiane jako Administratorzy na serwerze.</span><span class="sxs-lookup"><span data-stu-id="3c40e-115">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span>
<span data-ttu-id="3c40e-116">Użytkownicy lub grupy muszą być określeni jako format UPN, np. user@contoso.comgroups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="3c40e-116">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

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

### <span data-ttu-id="3c40e-117">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="3c40e-117">-BackupBlobContainerUri</span></span>
<span data-ttu-id="3c40e-118">Identyfikator URI kontenera obiektu BLOB na potrzeby tworzenia kopii zapasowych serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="3c40e-118">The blob container Uri for backup the Analysis Services server</span></span>

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

### <span data-ttu-id="3c40e-119">-DefaultConnectionMode</span><span class="sxs-lookup"><span data-stu-id="3c40e-119">-DefaultConnectionMode</span></span>
<span data-ttu-id="3c40e-120">Domyślny tryb połączenia serwera usługi Analysis Services</span><span class="sxs-lookup"><span data-stu-id="3c40e-120">Default connection mode of an Analysis service server</span></span>

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

### <span data-ttu-id="3c40e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c40e-121">-DefaultProfile</span></span>
<span data-ttu-id="3c40e-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3c40e-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c40e-123">-DisableBackup</span><span class="sxs-lookup"><span data-stu-id="3c40e-123">-DisableBackup</span></span>
<span data-ttu-id="3c40e-124">Przełącznik umożliwiający wyłączenie kontenera obiektu BLOB kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="3c40e-124">The switch to disable backup blob container.</span></span>
<span data-ttu-id="3c40e-125">Aby ponownie włączyć kontener obiektu BLOB kopii zapasowej, podaj identyfikator URI kontenera obiektów BLOB kopii zapasowej w postaci-BackupBlobContainerUri.</span><span class="sxs-lookup"><span data-stu-id="3c40e-125">To re-enable the backup blob container, please provide the backup blob container Uri as -BackupBlobContainerUri.</span></span>

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

### <span data-ttu-id="3c40e-126">-DisassociateGateway</span><span class="sxs-lookup"><span data-stu-id="3c40e-126">-DisassociateGateway</span></span>
<span data-ttu-id="3c40e-127">Usuwanie skojarzenia zasobu bramy z serwera analiz</span><span class="sxs-lookup"><span data-stu-id="3c40e-127">Disassociate Gateway resource from an Analysis server</span></span>

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

### <span data-ttu-id="3c40e-128">-FirewallConfig</span><span class="sxs-lookup"><span data-stu-id="3c40e-128">-FirewallConfig</span></span>
<span data-ttu-id="3c40e-129">Konfiguracja zapory serwera analiz</span><span class="sxs-lookup"><span data-stu-id="3c40e-129">Firewall config of an Analysis server</span></span>

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

### <span data-ttu-id="3c40e-130">-GatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="3c40e-130">-GatewayResourceId</span></span>
<span data-ttu-id="3c40e-131">Identyfikator zasobu bramy dla assocaite do serwera analizy</span><span class="sxs-lookup"><span data-stu-id="3c40e-131">Gateway resource Id for assocaite to an Analysis server</span></span>

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

### <span data-ttu-id="3c40e-132">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3c40e-132">-Name</span></span>
<span data-ttu-id="3c40e-133">Nazwa serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="3c40e-133">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="3c40e-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3c40e-134">-PassThru</span></span>
<span data-ttu-id="3c40e-135">Po pomyślnym zakończeniu operacji zwróci dane usuniętego serwera.</span><span class="sxs-lookup"><span data-stu-id="3c40e-135">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="3c40e-136">-ReadonlyReplicaCount</span><span class="sxs-lookup"><span data-stu-id="3c40e-136">-ReadonlyReplicaCount</span></span>
<span data-ttu-id="3c40e-137">Liczba replik tylko do odczytu serwera usługi Analysis Services</span><span class="sxs-lookup"><span data-stu-id="3c40e-137">Read only replica count of an Analysis service server</span></span>

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

### <span data-ttu-id="3c40e-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c40e-138">-ResourceGroupName</span></span>
<span data-ttu-id="3c40e-139">Nazwa grupy zasobów platformy Azure, do której należy serwer</span><span class="sxs-lookup"><span data-stu-id="3c40e-139">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="3c40e-140">-SKU</span><span class="sxs-lookup"><span data-stu-id="3c40e-140">-Sku</span></span>
<span data-ttu-id="3c40e-141">Nazwa jednostki SKU serwera.</span><span class="sxs-lookup"><span data-stu-id="3c40e-141">The name of the Sku for the server.</span></span>
<span data-ttu-id="3c40e-142">Obsługiwane wartości to 0 ', 1 ', 2 ', 4 ' dla warstwy standardowej; "B1"; "B2" dla warstwy podstawowej i 1 "dla warstwy rozwoju.</span><span class="sxs-lookup"><span data-stu-id="3c40e-142">The supported values are 'S0', 'S1', 'S2', 'S4' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

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

### <span data-ttu-id="3c40e-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="3c40e-143">-Tag</span></span>
<span data-ttu-id="3c40e-144">Pary klucz-wartość w formie tabeli skrótów ustawione jako znaczniki na serwerze.</span><span class="sxs-lookup"><span data-stu-id="3c40e-144">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

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

### <span data-ttu-id="3c40e-145">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3c40e-145">-Confirm</span></span>
<span data-ttu-id="3c40e-146">Monituje użytkownika o potwierdzenie, czy wykonać operację.</span><span class="sxs-lookup"><span data-stu-id="3c40e-146">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="3c40e-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c40e-147">-WhatIf</span></span>
<span data-ttu-id="3c40e-148">Opisuje akcje, które zostaną wykonane przez bieżącą operację bez ich rzeczywistego wykonywania.</span><span class="sxs-lookup"><span data-stu-id="3c40e-148">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="3c40e-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c40e-149">CommonParameters</span></span>
<span data-ttu-id="3c40e-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c40e-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c40e-151">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c40e-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c40e-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3c40e-152">INPUTS</span></span>

### <span data-ttu-id="3c40e-153">System. String</span><span class="sxs-lookup"><span data-stu-id="3c40e-153">System.String</span></span>

### <span data-ttu-id="3c40e-154">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="3c40e-154">System.Collections.Hashtable</span></span>

### <span data-ttu-id="3c40e-155">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3c40e-155">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="3c40e-156">System. Int32</span><span class="sxs-lookup"><span data-stu-id="3c40e-156">System.Int32</span></span>

### <span data-ttu-id="3c40e-157">Microsoft. Azure. Commands. AnalysisServices. models. PsAzureAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="3c40e-157">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="3c40e-158">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3c40e-158">OUTPUTS</span></span>

### <span data-ttu-id="3c40e-159">Microsoft. Azure. Commands. AnalysisServices. models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="3c40e-159">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="3c40e-160">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3c40e-160">NOTES</span></span>
<span data-ttu-id="3c40e-161">Alias: Set-AzureAs</span><span class="sxs-lookup"><span data-stu-id="3c40e-161">Alias: Set-AzureAs</span></span>

## <span data-ttu-id="3c40e-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3c40e-162">RELATED LINKS</span></span>

[<span data-ttu-id="3c40e-163">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="3c40e-163">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="3c40e-164">Remove-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="3c40e-164">Remove-AzureRmAnalysisServicesServer</span></span>](./Remove-AzureRmAnalysisServicesServer.md)
