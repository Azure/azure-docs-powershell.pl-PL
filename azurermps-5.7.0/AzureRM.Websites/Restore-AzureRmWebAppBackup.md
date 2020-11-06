---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: DC400E32-CAB9-4354-99B2-ABA4AA776030
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restore-azurermwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmWebAppBackup.md
ms.openlocfilehash: c68d9afb7c9498bbf734abcc376e6f123ebb8ac3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550439"
---
# <span data-ttu-id="f5e9b-101">Restore-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="f5e9b-101">Restore-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="f5e9b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f5e9b-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5e9b-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f5e9b-103">SYNTAX</span></span>

### <span data-ttu-id="f5e9b-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="f5e9b-104">FromResourceName</span></span>
```
Restore-AzureRmWebAppBackup [-Databases <DatabaseBackupSetting[]>] [-IgnoreConflictingHostNames]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite] [<CommonParameters>]
```

### <span data-ttu-id="f5e9b-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="f5e9b-105">FromWebApp</span></span>
```
Restore-AzureRmWebAppBackup [-Databases <DatabaseBackupSetting[]>] [-IgnoreConflictingHostNames]
 [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String> [-BlobName] <String>
 [-Overwrite] [<CommonParameters>]
```

## <span data-ttu-id="f5e9b-106">Opis</span><span class="sxs-lookup"><span data-stu-id="f5e9b-106">DESCRIPTION</span></span>
<span data-ttu-id="f5e9b-107">Polecenie cmdlet **Restore-AzureRmWebAppBackup** przywraca kopię zapasową aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="f5e9b-107">The **Restore-AzureRmWebAppBackup** cmdlet restores an Azure Web App Backup.</span></span>

## <span data-ttu-id="f5e9b-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f5e9b-108">EXAMPLES</span></span>

### <span data-ttu-id="f5e9b-109">1:1</span><span class="sxs-lookup"><span data-stu-id="f5e9b-109">1:</span></span>
```
PS C:\> Restore-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net" -BlobName "myBlob"
```

<span data-ttu-id="f5e9b-110">Przywraca kopię zapasową określonego ContosoWebApp aplikacji, która znajduje się w obszarze Domyślna grupa zasobów — sieć Web-zachód w obiekcie blob "obiekt BLOB" w lokalizacji https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="f5e9b-110">Restores a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in blob "myBlob" located at https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="f5e9b-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f5e9b-111">PARAMETERS</span></span>

### <span data-ttu-id="f5e9b-112">-Obiekt blobname</span><span class="sxs-lookup"><span data-stu-id="f5e9b-112">-BlobName</span></span>
<span data-ttu-id="f5e9b-113">Nazwa obiektu BLOB</span><span class="sxs-lookup"><span data-stu-id="f5e9b-113">Blob Name</span></span>

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

### <span data-ttu-id="f5e9b-114">-Bazy danych</span><span class="sxs-lookup"><span data-stu-id="f5e9b-114">-Databases</span></span>
<span data-ttu-id="f5e9b-115">Bazy danych typu DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="f5e9b-115">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="f5e9b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5e9b-116">-DefaultProfile</span></span>
<span data-ttu-id="f5e9b-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f5e9b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5e9b-118">-IgnoreConflictingHostNames</span><span class="sxs-lookup"><span data-stu-id="f5e9b-118">-IgnoreConflictingHostNames</span></span>
<span data-ttu-id="f5e9b-119">Ignorowanie opcji sprzecznych nazw hostów</span><span class="sxs-lookup"><span data-stu-id="f5e9b-119">Ignore Conflicting HostNames Option</span></span>

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

### <span data-ttu-id="f5e9b-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f5e9b-120">-Name</span></span>
<span data-ttu-id="f5e9b-121">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="f5e9b-121">WebApp Name</span></span>

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

### <span data-ttu-id="f5e9b-122">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="f5e9b-122">-Overwrite</span></span>
<span data-ttu-id="f5e9b-123">Opcja zastępowania</span><span class="sxs-lookup"><span data-stu-id="f5e9b-123">Overwrite Option</span></span>

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

### <span data-ttu-id="f5e9b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5e9b-124">-ResourceGroupName</span></span>
<span data-ttu-id="f5e9b-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="f5e9b-125">Resource Group Name</span></span>

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

### <span data-ttu-id="f5e9b-126">-Slot</span><span class="sxs-lookup"><span data-stu-id="f5e9b-126">-Slot</span></span>
<span data-ttu-id="f5e9b-127">Nazwa gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="f5e9b-127">WebApp Slot Name</span></span>

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

### <span data-ttu-id="f5e9b-128">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="f5e9b-128">-StorageAccountUrl</span></span>
<span data-ttu-id="f5e9b-129">Adres URL konta magazynu</span><span class="sxs-lookup"><span data-stu-id="f5e9b-129">Storage Account Url</span></span>

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

### <span data-ttu-id="f5e9b-130">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="f5e9b-130">-WebApp</span></span>
<span data-ttu-id="f5e9b-131">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="f5e9b-131">WebApp Object</span></span>

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

### <span data-ttu-id="f5e9b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5e9b-132">CommonParameters</span></span>
<span data-ttu-id="f5e9b-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5e9b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5e9b-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5e9b-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5e9b-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f5e9b-135">INPUTS</span></span>

### <span data-ttu-id="f5e9b-136">Klienta</span><span class="sxs-lookup"><span data-stu-id="f5e9b-136">Site</span></span>
<span data-ttu-id="f5e9b-137">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="f5e9b-137">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="f5e9b-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f5e9b-138">OUTPUTS</span></span>

## <span data-ttu-id="f5e9b-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f5e9b-139">NOTES</span></span>

## <span data-ttu-id="f5e9b-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f5e9b-140">RELATED LINKS</span></span>

