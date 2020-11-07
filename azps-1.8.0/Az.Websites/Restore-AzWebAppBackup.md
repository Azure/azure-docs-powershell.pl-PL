---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: DC400E32-CAB9-4354-99B2-ABA4AA776030
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restore-azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzWebAppBackup.md
ms.openlocfilehash: 94fbc71db34ca0abc6a27130dc166318794e271a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707269"
---
# <span data-ttu-id="dffd6-101">Restore-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="dffd6-101">Restore-AzWebAppBackup</span></span>

## <span data-ttu-id="dffd6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dffd6-102">SYNOPSIS</span></span>

## <span data-ttu-id="dffd6-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dffd6-103">SYNTAX</span></span>

### <span data-ttu-id="dffd6-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="dffd6-104">FromResourceName</span></span>
```
Restore-AzWebAppBackup [-AppServicePlan <String>] [-Databases <DatabaseBackupSetting[]>]
 [-IgnoreConflictingHostNames] [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite]
 [<CommonParameters>]
```

### <span data-ttu-id="dffd6-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="dffd6-105">FromWebApp</span></span>
```
Restore-AzWebAppBackup [-AppServicePlan <String>] [-Databases <DatabaseBackupSetting[]>]
 [-IgnoreConflictingHostNames] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite] [<CommonParameters>]
```

## <span data-ttu-id="dffd6-106">Opis</span><span class="sxs-lookup"><span data-stu-id="dffd6-106">DESCRIPTION</span></span>
<span data-ttu-id="dffd6-107">Polecenie cmdlet **Restore-AzWebAppBackup** przywraca kopię zapasową aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="dffd6-107">The **Restore-AzWebAppBackup** cmdlet restores an Azure Web App Backup.</span></span>

## <span data-ttu-id="dffd6-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dffd6-108">EXAMPLES</span></span>

### <span data-ttu-id="dffd6-109">1:1</span><span class="sxs-lookup"><span data-stu-id="dffd6-109">1:</span></span>
```
PS C:\> Restore-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net" -BlobName "myBlob"
```

<span data-ttu-id="dffd6-110">Przywraca kopię zapasową określonego ContosoWebApp aplikacji, która znajduje się w obszarze Domyślna grupa zasobów — sieć Web-zachód w obiekcie blob "obiekt BLOB" w lokalizacji https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="dffd6-110">Restores a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in blob "myBlob" located at https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="dffd6-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dffd6-111">PARAMETERS</span></span>

### <span data-ttu-id="dffd6-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="dffd6-112">-AppServicePlan</span></span>
<span data-ttu-id="dffd6-113">Nazwa planu usługi App Service dla przywróconej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="dffd6-113">The name of the App Service Plan for the restored app.</span></span> <span data-ttu-id="dffd6-114">Jeśli to pole pozostanie puste, zostanie wykorzystany bieżący plan usługi App Service.</span><span class="sxs-lookup"><span data-stu-id="dffd6-114">If left empty, the app's current App Service Plan is used.</span></span>

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

### <span data-ttu-id="dffd6-115">-Obiekt blobname</span><span class="sxs-lookup"><span data-stu-id="dffd6-115">-BlobName</span></span>
<span data-ttu-id="dffd6-116">Nazwa obiektu BLOB</span><span class="sxs-lookup"><span data-stu-id="dffd6-116">Blob Name</span></span>

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

### <span data-ttu-id="dffd6-117">-Bazy danych</span><span class="sxs-lookup"><span data-stu-id="dffd6-117">-Databases</span></span>
<span data-ttu-id="dffd6-118">Bazy danych typu DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="dffd6-118">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="dffd6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dffd6-119">-DefaultProfile</span></span>
<span data-ttu-id="dffd6-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dffd6-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dffd6-121">-IgnoreConflictingHostNames</span><span class="sxs-lookup"><span data-stu-id="dffd6-121">-IgnoreConflictingHostNames</span></span>
<span data-ttu-id="dffd6-122">Ignorowanie opcji sprzecznych nazw hostów</span><span class="sxs-lookup"><span data-stu-id="dffd6-122">Ignore Conflicting HostNames Option</span></span>

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

### <span data-ttu-id="dffd6-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dffd6-123">-Name</span></span>
<span data-ttu-id="dffd6-124">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="dffd6-124">WebApp Name</span></span>

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

### <span data-ttu-id="dffd6-125">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="dffd6-125">-Overwrite</span></span>
<span data-ttu-id="dffd6-126">Opcja zastępowania</span><span class="sxs-lookup"><span data-stu-id="dffd6-126">Overwrite Option</span></span>

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

### <span data-ttu-id="dffd6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dffd6-127">-ResourceGroupName</span></span>
<span data-ttu-id="dffd6-128">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="dffd6-128">Resource Group Name</span></span>

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

### <span data-ttu-id="dffd6-129">-Slot</span><span class="sxs-lookup"><span data-stu-id="dffd6-129">-Slot</span></span>
<span data-ttu-id="dffd6-130">Nazwa gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="dffd6-130">WebApp Slot Name</span></span>

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

### <span data-ttu-id="dffd6-131">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="dffd6-131">-StorageAccountUrl</span></span>
<span data-ttu-id="dffd6-132">Adres URL konta magazynu</span><span class="sxs-lookup"><span data-stu-id="dffd6-132">Storage Account Url</span></span>

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

### <span data-ttu-id="dffd6-133">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="dffd6-133">-WebApp</span></span>
<span data-ttu-id="dffd6-134">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="dffd6-134">WebApp Object</span></span>

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

### <span data-ttu-id="dffd6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dffd6-135">CommonParameters</span></span>
<span data-ttu-id="dffd6-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dffd6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dffd6-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dffd6-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dffd6-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dffd6-138">INPUTS</span></span>

### <span data-ttu-id="dffd6-139">System. String</span><span class="sxs-lookup"><span data-stu-id="dffd6-139">System.String</span></span>

### <span data-ttu-id="dffd6-140">Microsoft. Azure. Management. Web. MODELES. DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="dffd6-140">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]</span></span>

### <span data-ttu-id="dffd6-141">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="dffd6-141">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="dffd6-142">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="dffd6-142">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="dffd6-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dffd6-143">OUTPUTS</span></span>

### <span data-ttu-id="dffd6-144">System. void</span><span class="sxs-lookup"><span data-stu-id="dffd6-144">System.Void</span></span>

## <span data-ttu-id="dffd6-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dffd6-145">NOTES</span></span>

## <span data-ttu-id="dffd6-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dffd6-146">RELATED LINKS</span></span>
