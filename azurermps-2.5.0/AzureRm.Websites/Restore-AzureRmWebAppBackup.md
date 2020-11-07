---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: DC400E32-CAB9-4354-99B2-ABA4AA776030
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restore-azurermwebappbackup
schema: 2.0.0
ms.openlocfilehash: 9c28d9235eefe6c4f33537115b548137c5bc6c88
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899018"
---
# <span data-ttu-id="13bfe-101">Restore-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="13bfe-101">Restore-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="13bfe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="13bfe-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13bfe-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="13bfe-103">SYNTAX</span></span>

### <span data-ttu-id="13bfe-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="13bfe-104">FromResourceName</span></span>
```
Restore-AzureRmWebAppBackup [-AppServicePlan <String>] [-Databases <DatabaseBackupSetting[]>]
 [-IgnoreConflictingHostNames] [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite]
 [<CommonParameters>]
```

### <span data-ttu-id="13bfe-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="13bfe-105">FromWebApp</span></span>
```
Restore-AzureRmWebAppBackup [-AppServicePlan <String>] [-Databases <DatabaseBackupSetting[]>]
 [-IgnoreConflictingHostNames] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite] [<CommonParameters>]
```

## <span data-ttu-id="13bfe-106">Opis</span><span class="sxs-lookup"><span data-stu-id="13bfe-106">DESCRIPTION</span></span>
<span data-ttu-id="13bfe-107">Polecenie cmdlet **Restore-AzureRmWebAppBackup** przywraca kopię zapasową aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="13bfe-107">The **Restore-AzureRmWebAppBackup** cmdlet restores an Azure Web App Backup.</span></span>

## <span data-ttu-id="13bfe-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="13bfe-108">EXAMPLES</span></span>

### <span data-ttu-id="13bfe-109">1:1</span><span class="sxs-lookup"><span data-stu-id="13bfe-109">1:</span></span>
```
PS C:\> Restore-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net" -BlobName "myBlob"
```

<span data-ttu-id="13bfe-110">Przywraca kopię zapasową określonego ContosoWebApp aplikacji, która znajduje się w obszarze Domyślna grupa zasobów — sieć Web-zachód w obiekcie blob "obiekt BLOB" w lokalizacji https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="13bfe-110">Restores a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in blob "myBlob" located at https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="13bfe-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="13bfe-111">PARAMETERS</span></span>

### <span data-ttu-id="13bfe-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="13bfe-112">-AppServicePlan</span></span>
<span data-ttu-id="13bfe-113">Nazwa planu usługi App Service dla przywróconej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="13bfe-113">The name of the App Service Plan for the restored app.</span></span> <span data-ttu-id="13bfe-114">Jeśli to pole pozostanie puste, zostanie wykorzystany bieżący plan usługi App Service.</span><span class="sxs-lookup"><span data-stu-id="13bfe-114">If left empty, the app's current App Service Plan is used.</span></span>
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

### <span data-ttu-id="13bfe-115">-Obiekt blobname</span><span class="sxs-lookup"><span data-stu-id="13bfe-115">-BlobName</span></span>
<span data-ttu-id="13bfe-116">Nazwa obiektu BLOB</span><span class="sxs-lookup"><span data-stu-id="13bfe-116">Blob Name</span></span>

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

### <span data-ttu-id="13bfe-117">-Bazy danych</span><span class="sxs-lookup"><span data-stu-id="13bfe-117">-Databases</span></span>
<span data-ttu-id="13bfe-118">Bazy danych typu DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="13bfe-118">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="13bfe-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13bfe-119">-DefaultProfile</span></span>
<span data-ttu-id="13bfe-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="13bfe-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13bfe-121">-IgnoreConflictingHostNames</span><span class="sxs-lookup"><span data-stu-id="13bfe-121">-IgnoreConflictingHostNames</span></span>
<span data-ttu-id="13bfe-122">Ignorowanie opcji sprzecznych nazw hostów</span><span class="sxs-lookup"><span data-stu-id="13bfe-122">Ignore Conflicting HostNames Option</span></span>

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

### <span data-ttu-id="13bfe-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="13bfe-123">-Name</span></span>
<span data-ttu-id="13bfe-124">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="13bfe-124">WebApp Name</span></span>

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

### <span data-ttu-id="13bfe-125">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="13bfe-125">-Overwrite</span></span>
<span data-ttu-id="13bfe-126">Opcja zastępowania</span><span class="sxs-lookup"><span data-stu-id="13bfe-126">Overwrite Option</span></span>

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

### <span data-ttu-id="13bfe-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13bfe-127">-ResourceGroupName</span></span>
<span data-ttu-id="13bfe-128">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="13bfe-128">Resource Group Name</span></span>

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

### <span data-ttu-id="13bfe-129">-Slot</span><span class="sxs-lookup"><span data-stu-id="13bfe-129">-Slot</span></span>
<span data-ttu-id="13bfe-130">Nazwa gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="13bfe-130">WebApp Slot Name</span></span>

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

### <span data-ttu-id="13bfe-131">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="13bfe-131">-StorageAccountUrl</span></span>
<span data-ttu-id="13bfe-132">Adres URL konta magazynu</span><span class="sxs-lookup"><span data-stu-id="13bfe-132">Storage Account Url</span></span>

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

### <span data-ttu-id="13bfe-133">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="13bfe-133">-WebApp</span></span>
<span data-ttu-id="13bfe-134">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="13bfe-134">WebApp Object</span></span>

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

### <span data-ttu-id="13bfe-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13bfe-135">CommonParameters</span></span>
<span data-ttu-id="13bfe-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13bfe-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13bfe-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13bfe-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13bfe-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="13bfe-138">INPUTS</span></span>

### <span data-ttu-id="13bfe-139">Klienta</span><span class="sxs-lookup"><span data-stu-id="13bfe-139">Site</span></span>
<span data-ttu-id="13bfe-140">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="13bfe-140">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="13bfe-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="13bfe-141">OUTPUTS</span></span>

## <span data-ttu-id="13bfe-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="13bfe-142">NOTES</span></span>

## <span data-ttu-id="13bfe-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="13bfe-143">RELATED LINKS</span></span>

