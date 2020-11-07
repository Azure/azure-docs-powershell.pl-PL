---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: DC400E32-CAB9-4354-99B2-ABA4AA776030
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/restore-Azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Restore-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Restore-AzWebAppBackup.md
ms.openlocfilehash: f93a173e79cb34c5603ce58fc3e03c92869a5d01
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891837"
---
# <span data-ttu-id="51e48-101">Restore-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="51e48-101">Restore-AzWebAppBackup</span></span>

## <span data-ttu-id="51e48-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="51e48-102">SYNOPSIS</span></span>

## <span data-ttu-id="51e48-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="51e48-103">SYNTAX</span></span>

### <span data-ttu-id="51e48-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="51e48-104">FromResourceName</span></span>
```
Restore-AzWebAppBackup [-AppServicePlan <String>] [-Databases <DatabaseBackupSetting[]>]
 [-IgnoreConflictingHostNames] [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite]
 [<CommonParameters>]
```

### <span data-ttu-id="51e48-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="51e48-105">FromWebApp</span></span>
```
Restore-AzWebAppBackup [-AppServicePlan <String>] [-Databases <DatabaseBackupSetting[]>]
 [-IgnoreConflictingHostNames] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite] [<CommonParameters>]
```

## <span data-ttu-id="51e48-106">Opis</span><span class="sxs-lookup"><span data-stu-id="51e48-106">DESCRIPTION</span></span>
<span data-ttu-id="51e48-107">Polecenie cmdlet **Restore-AzWebAppBackup** przywraca kopię zapasową aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="51e48-107">The **Restore-AzWebAppBackup** cmdlet restores an Azure Web App Backup.</span></span>

## <span data-ttu-id="51e48-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="51e48-108">EXAMPLES</span></span>

### <span data-ttu-id="51e48-109">1:1</span><span class="sxs-lookup"><span data-stu-id="51e48-109">1:</span></span>
```
PS C:\> Restore-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net" -BlobName "myBlob"
```

<span data-ttu-id="51e48-110">Przywraca kopię zapasową określonego ContosoWebApp aplikacji, która znajduje się w obszarze Domyślna grupa zasobów — sieć Web-zachód w obiekcie blob "obiekt BLOB" w lokalizacji https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="51e48-110">Restores a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in blob "myBlob" located at https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="51e48-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="51e48-111">PARAMETERS</span></span>

### <span data-ttu-id="51e48-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="51e48-112">-AppServicePlan</span></span>
<span data-ttu-id="51e48-113">Nazwa planu usługi App Service dla przywróconej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="51e48-113">The name of the App Service Plan for the restored app.</span></span> <span data-ttu-id="51e48-114">Jeśli to pole pozostanie puste, zostanie wykorzystany bieżący plan usługi App Service.</span><span class="sxs-lookup"><span data-stu-id="51e48-114">If left empty, the app's current App Service Plan is used.</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51e48-115">-Obiekt blobname</span><span class="sxs-lookup"><span data-stu-id="51e48-115">-BlobName</span></span>
<span data-ttu-id="51e48-116">Nazwa obiektu BLOB</span><span class="sxs-lookup"><span data-stu-id="51e48-116">Blob Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51e48-117">-Bazy danych</span><span class="sxs-lookup"><span data-stu-id="51e48-117">-Databases</span></span>
<span data-ttu-id="51e48-118">Bazy danych typu DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="51e48-118">Databases of type DatabaseBackupSetting[]</span></span>

```yaml
Type: DatabaseBackupSetting[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51e48-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51e48-119">-DefaultProfile</span></span>
<span data-ttu-id="51e48-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="51e48-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51e48-121">-IgnoreConflictingHostNames</span><span class="sxs-lookup"><span data-stu-id="51e48-121">-IgnoreConflictingHostNames</span></span>
<span data-ttu-id="51e48-122">Ignorowanie opcji sprzecznych nazw hostów</span><span class="sxs-lookup"><span data-stu-id="51e48-122">Ignore Conflicting HostNames Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51e48-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="51e48-123">-Name</span></span>
<span data-ttu-id="51e48-124">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="51e48-124">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51e48-125">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="51e48-125">-Overwrite</span></span>
<span data-ttu-id="51e48-126">Opcja zastępowania</span><span class="sxs-lookup"><span data-stu-id="51e48-126">Overwrite Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51e48-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51e48-127">-ResourceGroupName</span></span>
<span data-ttu-id="51e48-128">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="51e48-128">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51e48-129">-Slot</span><span class="sxs-lookup"><span data-stu-id="51e48-129">-Slot</span></span>
<span data-ttu-id="51e48-130">Nazwa gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="51e48-130">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51e48-131">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="51e48-131">-StorageAccountUrl</span></span>
<span data-ttu-id="51e48-132">Adres URL konta magazynu</span><span class="sxs-lookup"><span data-stu-id="51e48-132">Storage Account Url</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51e48-133">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="51e48-133">-WebApp</span></span>
<span data-ttu-id="51e48-134">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="51e48-134">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51e48-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51e48-135">CommonParameters</span></span>
<span data-ttu-id="51e48-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51e48-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51e48-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51e48-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51e48-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="51e48-138">INPUTS</span></span>

### <span data-ttu-id="51e48-139">Klienta</span><span class="sxs-lookup"><span data-stu-id="51e48-139">Site</span></span>
<span data-ttu-id="51e48-140">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="51e48-140">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="51e48-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="51e48-141">OUTPUTS</span></span>

## <span data-ttu-id="51e48-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="51e48-142">NOTES</span></span>

## <span data-ttu-id="51e48-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="51e48-143">RELATED LINKS</span></span>

