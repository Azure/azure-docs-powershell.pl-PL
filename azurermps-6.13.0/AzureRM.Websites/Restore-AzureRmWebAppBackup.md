---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: DC400E32-CAB9-4354-99B2-ABA4AA776030
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restore-azurermwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmWebAppBackup.md
ms.openlocfilehash: efb570c22b5345b9d75fdf96dca061dc5cf7847f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546303"
---
# <span data-ttu-id="912d3-101">Restore-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="912d3-101">Restore-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="912d3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="912d3-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="912d3-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="912d3-103">SYNTAX</span></span>

### <span data-ttu-id="912d3-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="912d3-104">FromResourceName</span></span>
```
Restore-AzureRmWebAppBackup [-AppServicePlan <String>] [-Databases <DatabaseBackupSetting[]>]
 [-IgnoreConflictingHostNames] [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite]
 [<CommonParameters>]
```

### <span data-ttu-id="912d3-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="912d3-105">FromWebApp</span></span>
```
Restore-AzureRmWebAppBackup [-AppServicePlan <String>] [-Databases <DatabaseBackupSetting[]>]
 [-IgnoreConflictingHostNames] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite] [<CommonParameters>]
```

## <span data-ttu-id="912d3-106">Opis</span><span class="sxs-lookup"><span data-stu-id="912d3-106">DESCRIPTION</span></span>
<span data-ttu-id="912d3-107">Polecenie cmdlet **Restore-AzureRmWebAppBackup** przywraca kopię zapasową aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="912d3-107">The **Restore-AzureRmWebAppBackup** cmdlet restores an Azure Web App Backup.</span></span>

## <span data-ttu-id="912d3-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="912d3-108">EXAMPLES</span></span>

### <span data-ttu-id="912d3-109">1:1</span><span class="sxs-lookup"><span data-stu-id="912d3-109">1:</span></span>
```
PS C:\> Restore-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net" -BlobName "myBlob"
```

<span data-ttu-id="912d3-110">Przywraca kopię zapasową określonego ContosoWebApp aplikacji, która znajduje się w obszarze Domyślna grupa zasobów — sieć Web-zachód w obiekcie blob "obiekt BLOB" w lokalizacji https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="912d3-110">Restores a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in blob "myBlob" located at https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="912d3-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="912d3-111">PARAMETERS</span></span>

### <span data-ttu-id="912d3-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="912d3-112">-AppServicePlan</span></span>
<span data-ttu-id="912d3-113">Nazwa planu usługi App Service dla przywróconej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="912d3-113">The name of the App Service Plan for the restored app.</span></span> <span data-ttu-id="912d3-114">Jeśli to pole pozostanie puste, zostanie wykorzystany bieżący plan usługi App Service.</span><span class="sxs-lookup"><span data-stu-id="912d3-114">If left empty, the app's current App Service Plan is used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="912d3-115">-Obiekt blobname</span><span class="sxs-lookup"><span data-stu-id="912d3-115">-BlobName</span></span>
<span data-ttu-id="912d3-116">Nazwa obiektu BLOB</span><span class="sxs-lookup"><span data-stu-id="912d3-116">Blob Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="912d3-117">-Bazy danych</span><span class="sxs-lookup"><span data-stu-id="912d3-117">-Databases</span></span>
<span data-ttu-id="912d3-118">Bazy danych typu DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="912d3-118">Databases of type DatabaseBackupSetting[]</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="912d3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="912d3-119">-DefaultProfile</span></span>
<span data-ttu-id="912d3-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="912d3-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="912d3-121">-IgnoreConflictingHostNames</span><span class="sxs-lookup"><span data-stu-id="912d3-121">-IgnoreConflictingHostNames</span></span>
<span data-ttu-id="912d3-122">Ignorowanie opcji sprzecznych nazw hostów</span><span class="sxs-lookup"><span data-stu-id="912d3-122">Ignore Conflicting HostNames Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="912d3-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="912d3-123">-Name</span></span>
<span data-ttu-id="912d3-124">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="912d3-124">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="912d3-125">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="912d3-125">-Overwrite</span></span>
<span data-ttu-id="912d3-126">Opcja zastępowania</span><span class="sxs-lookup"><span data-stu-id="912d3-126">Overwrite Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="912d3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="912d3-127">-ResourceGroupName</span></span>
<span data-ttu-id="912d3-128">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="912d3-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="912d3-129">-Slot</span><span class="sxs-lookup"><span data-stu-id="912d3-129">-Slot</span></span>
<span data-ttu-id="912d3-130">Nazwa gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="912d3-130">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="912d3-131">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="912d3-131">-StorageAccountUrl</span></span>
<span data-ttu-id="912d3-132">Adres URL konta magazynu</span><span class="sxs-lookup"><span data-stu-id="912d3-132">Storage Account Url</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="912d3-133">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="912d3-133">-WebApp</span></span>
<span data-ttu-id="912d3-134">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="912d3-134">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: FromWebApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="912d3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="912d3-135">CommonParameters</span></span>
<span data-ttu-id="912d3-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="912d3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="912d3-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="912d3-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="912d3-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="912d3-138">INPUTS</span></span>

### <span data-ttu-id="912d3-139">System. String</span><span class="sxs-lookup"><span data-stu-id="912d3-139">System.String</span></span>

### <span data-ttu-id="912d3-140">Microsoft. Azure. Management. Web. MODELES. DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="912d3-140">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]</span></span>

### <span data-ttu-id="912d3-141">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="912d3-141">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="912d3-142">Microsoft. Azure. Management. Web. models. site</span><span class="sxs-lookup"><span data-stu-id="912d3-142">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="912d3-143">Parametry: aplikacji (ByValue)</span><span class="sxs-lookup"><span data-stu-id="912d3-143">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="912d3-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="912d3-144">OUTPUTS</span></span>

### <span data-ttu-id="912d3-145">System. void</span><span class="sxs-lookup"><span data-stu-id="912d3-145">System.Void</span></span>

## <span data-ttu-id="912d3-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="912d3-146">NOTES</span></span>

## <span data-ttu-id="912d3-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="912d3-147">RELATED LINKS</span></span>
