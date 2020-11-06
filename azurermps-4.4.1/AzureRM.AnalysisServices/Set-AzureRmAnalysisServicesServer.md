---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Set-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Set-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 6bda63ad0c8e900a73c0ccd2afc506be7feae908
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525829"
---
# <span data-ttu-id="2ebbf-101">Set-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="2ebbf-101">Set-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="2ebbf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2ebbf-102">SYNOPSIS</span></span>
<span data-ttu-id="2ebbf-103">Modyfikowanie wystąpienia serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="2ebbf-103">Modifies  an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ebbf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2ebbf-104">SYNTAX</span></span>

### <span data-ttu-id="2ebbf-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="2ebbf-105">Default (Default)</span></span>
```
Set-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ebbf-106">Wyłączanie kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="2ebbf-106">Disable Backup</span></span>
```
Set-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-DisableBackup]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ebbf-107">Opis</span><span class="sxs-lookup"><span data-stu-id="2ebbf-107">DESCRIPTION</span></span>
<span data-ttu-id="2ebbf-108">Polecenie cmdlet Set-AzureRmAnalysisServicesServer modyfikuje wystąpienie serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="2ebbf-108">The Set-AzureRmAnalysisServicesServer cmdlet modifies an instance of Analysis Services server</span></span>

## <span data-ttu-id="2ebbf-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2ebbf-109">EXAMPLES</span></span>

### <span data-ttu-id="2ebbf-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2ebbf-110">Example 1</span></span>
```
PS C:\> Set-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup" -Tag "key1:value1,key2:value2" -Administrator "testuser1@contoso.com"
```

<span data-ttu-id="2ebbf-111">Modyfikuje serwer o nazwie TestServer w zbiorze testerów zasobów, aby ustawić Tagi jako KEY1: wartość1 i key2: wartość2 i administrator, aby testuser1@contoso.com</span><span class="sxs-lookup"><span data-stu-id="2ebbf-111">Modifies the server named testserver in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com</span></span>

## <span data-ttu-id="2ebbf-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2ebbf-112">PARAMETERS</span></span>

### <span data-ttu-id="2ebbf-113">-Administrator</span><span class="sxs-lookup"><span data-stu-id="2ebbf-113">-Administrator</span></span>
<span data-ttu-id="2ebbf-114">Ciąg reprezentujący rozdzielaną przecinkami listę użytkowników lub grup, które mają być ustawiane jako Administratorzy na serwerze.</span><span class="sxs-lookup"><span data-stu-id="2ebbf-114">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span>
<span data-ttu-id="2ebbf-115">Użytkownicy lub grupy muszą być określeni jako format UPN, np. user@contoso.comgroups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="2ebbf-115">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

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

### <span data-ttu-id="2ebbf-116">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="2ebbf-116">-BackupBlobContainerUri</span></span>
<span data-ttu-id="2ebbf-117">Identyfikator URI kontenera obiektu BLOB na potrzeby tworzenia kopii zapasowych serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="2ebbf-117">The blob container Uri for backup the Analysis Services server</span></span>

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

### <span data-ttu-id="2ebbf-118">-DisableBackup</span><span class="sxs-lookup"><span data-stu-id="2ebbf-118">-DisableBackup</span></span>
<span data-ttu-id="2ebbf-119">Przełącznik umożliwiający wyłączenie kontenera obiektu BLOB kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="2ebbf-119">The switch to disable backup blob container.</span></span>
<span data-ttu-id="2ebbf-120">Aby ponownie włączyć kontener obiektu BLOB kopii zapasowej, podaj identyfikator URI kontenera obiektów BLOB kopii zapasowej w postaci-BackupBlobContainerUri.</span><span class="sxs-lookup"><span data-stu-id="2ebbf-120">To re-enable the backup blob container, please provide the backup blob container Uri as -BackupBlobContainerUri.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Disable Backup
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ebbf-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2ebbf-121">-Name</span></span>
<span data-ttu-id="2ebbf-122">Nazwa serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="2ebbf-122">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="2ebbf-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2ebbf-123">-PassThru</span></span>
<span data-ttu-id="2ebbf-124">Po pomyślnym zakończeniu operacji zwróci dane usuniętego serwera.</span><span class="sxs-lookup"><span data-stu-id="2ebbf-124">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="2ebbf-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ebbf-125">-ResourceGroupName</span></span>
<span data-ttu-id="2ebbf-126">Nazwa grupy zasobów platformy Azure, do której należy serwer</span><span class="sxs-lookup"><span data-stu-id="2ebbf-126">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="2ebbf-127">-SKU</span><span class="sxs-lookup"><span data-stu-id="2ebbf-127">-Sku</span></span>
<span data-ttu-id="2ebbf-128">Nazwa jednostki SKU serwera.</span><span class="sxs-lookup"><span data-stu-id="2ebbf-128">The name of the Sku for the server.</span></span>
<span data-ttu-id="2ebbf-129">Obsługiwane wartości to 0 ', 1 ', 2 ', 4 ' dla warstwy standardowej; "B1"; "B2" dla warstwy podstawowej i 1 "dla warstwy rozwoju.</span><span class="sxs-lookup"><span data-stu-id="2ebbf-129">The supported values are 'S0', 'S1', 'S2', 'S4' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

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

### <span data-ttu-id="2ebbf-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="2ebbf-130">-Tag</span></span>
<span data-ttu-id="2ebbf-131">Pary klucz-wartość w formie tabeli skrótów ustawione jako znaczniki na serwerze.</span><span class="sxs-lookup"><span data-stu-id="2ebbf-131">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

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

### <span data-ttu-id="2ebbf-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2ebbf-132">-Confirm</span></span>
<span data-ttu-id="2ebbf-133">Monituje użytkownika o potwierdzenie, czy wykonać operację.</span><span class="sxs-lookup"><span data-stu-id="2ebbf-133">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="2ebbf-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ebbf-134">-WhatIf</span></span>
<span data-ttu-id="2ebbf-135">Opisuje akcje, które zostaną wykonane przez bieżącą operację bez ich rzeczywistego wykonywania.</span><span class="sxs-lookup"><span data-stu-id="2ebbf-135">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="2ebbf-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ebbf-136">-DefaultProfile</span></span>
<span data-ttu-id="2ebbf-137">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2ebbf-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ebbf-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ebbf-138">CommonParameters</span></span>
<span data-ttu-id="2ebbf-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ebbf-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ebbf-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ebbf-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ebbf-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2ebbf-141">INPUTS</span></span>

## <span data-ttu-id="2ebbf-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2ebbf-142">OUTPUTS</span></span>

### <span data-ttu-id="2ebbf-143">Microsoft. Azure. Management. Analysis. MODELES. AnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="2ebbf-143">Microsoft.Azure.Management.Analysis.Models.AnalysisServicesServer</span></span>

## <span data-ttu-id="2ebbf-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2ebbf-144">NOTES</span></span>
<span data-ttu-id="2ebbf-145">Alias: Set-AzureAs</span><span class="sxs-lookup"><span data-stu-id="2ebbf-145">Alias: Set-AzureAs</span></span>

## <span data-ttu-id="2ebbf-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2ebbf-146">RELATED LINKS</span></span>

[<span data-ttu-id="2ebbf-147">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="2ebbf-147">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="2ebbf-148">Remove-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="2ebbf-148">Remove-AzureRmAnalysisServicesServer</span></span>](./Remove-AzureRmAnalysisServicesServer.md)
