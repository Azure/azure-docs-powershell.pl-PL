---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: DC400E32-CAB9-4354-99B2-ABA4AA776030
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmWebAppBackup.md
ms.openlocfilehash: 07cf4daffeaf00c516bc5b179e5f4a2133a2c4ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525446"
---
# <span data-ttu-id="57d8e-101">Restore-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="57d8e-101">Restore-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="57d8e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="57d8e-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57d8e-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="57d8e-103">SYNTAX</span></span>

### <span data-ttu-id="57d8e-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="57d8e-104">FromResourceName</span></span>
```
Restore-AzureRmWebAppBackup [-Databases <DatabaseBackupSetting[]>] [-IgnoreConflictingHostNames]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite] [<CommonParameters>]
```

### <span data-ttu-id="57d8e-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="57d8e-105">FromWebApp</span></span>
```
Restore-AzureRmWebAppBackup [-Databases <DatabaseBackupSetting[]>] [-IgnoreConflictingHostNames]
 [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String> [-BlobName] <String>
 [-Overwrite] [<CommonParameters>]
```

## <span data-ttu-id="57d8e-106">Opis</span><span class="sxs-lookup"><span data-stu-id="57d8e-106">DESCRIPTION</span></span>
<span data-ttu-id="57d8e-107">Polecenie cmdlet **Restore-AzureRmWebAppBackup** przywraca kopię zapasową aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="57d8e-107">The **Restore-AzureRmWebAppBackup** cmdlet restores an Azure Web App Backup.</span></span>

## <span data-ttu-id="57d8e-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="57d8e-108">EXAMPLES</span></span>

### <span data-ttu-id="57d8e-109">1:1</span><span class="sxs-lookup"><span data-stu-id="57d8e-109">1:</span></span>
```
PS C:\> Restore-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net" -BlobName "myBlob"
```

<span data-ttu-id="57d8e-110">Przywraca kopię zapasową określonego ContosoWebApp aplikacji, która znajduje się w obszarze Domyślna grupa zasobów — sieć Web-zachód w obiekcie blob "obiekt BLOB" w lokalizacji https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="57d8e-110">Restores a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in blob "myBlob" located at https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="57d8e-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="57d8e-111">PARAMETERS</span></span>

### <span data-ttu-id="57d8e-112">-Obiekt blobname</span><span class="sxs-lookup"><span data-stu-id="57d8e-112">-BlobName</span></span>
<span data-ttu-id="57d8e-113">Nazwa obiektu BLOB</span><span class="sxs-lookup"><span data-stu-id="57d8e-113">Blob Name</span></span>

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

### <span data-ttu-id="57d8e-114">-Bazy danych</span><span class="sxs-lookup"><span data-stu-id="57d8e-114">-Databases</span></span>
<span data-ttu-id="57d8e-115">Bazy danych typu DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="57d8e-115">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="57d8e-116">-IgnoreConflictingHostNames</span><span class="sxs-lookup"><span data-stu-id="57d8e-116">-IgnoreConflictingHostNames</span></span>
<span data-ttu-id="57d8e-117">Ignorowanie opcji sprzecznych nazw hostów</span><span class="sxs-lookup"><span data-stu-id="57d8e-117">Ignore Conflicting HostNames Option</span></span>

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

### <span data-ttu-id="57d8e-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="57d8e-118">-Name</span></span>
<span data-ttu-id="57d8e-119">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="57d8e-119">WebApp Name</span></span>

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

### <span data-ttu-id="57d8e-120">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="57d8e-120">-Overwrite</span></span>
<span data-ttu-id="57d8e-121">Opcja zastępowania</span><span class="sxs-lookup"><span data-stu-id="57d8e-121">Overwrite Option</span></span>

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

### <span data-ttu-id="57d8e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57d8e-122">-ResourceGroupName</span></span>
<span data-ttu-id="57d8e-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="57d8e-123">Resource Group Name</span></span>

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

### <span data-ttu-id="57d8e-124">-Slot</span><span class="sxs-lookup"><span data-stu-id="57d8e-124">-Slot</span></span>
<span data-ttu-id="57d8e-125">Nazwa gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="57d8e-125">WebApp Slot Name</span></span>

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

### <span data-ttu-id="57d8e-126">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="57d8e-126">-StorageAccountUrl</span></span>
<span data-ttu-id="57d8e-127">Adres URL konta magazynu</span><span class="sxs-lookup"><span data-stu-id="57d8e-127">Storage Account Url</span></span>

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

### <span data-ttu-id="57d8e-128">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="57d8e-128">-WebApp</span></span>
<span data-ttu-id="57d8e-129">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="57d8e-129">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57d8e-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57d8e-130">-DefaultProfile</span></span>
<span data-ttu-id="57d8e-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="57d8e-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57d8e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57d8e-132">CommonParameters</span></span>
<span data-ttu-id="57d8e-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57d8e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57d8e-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57d8e-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57d8e-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="57d8e-135">INPUTS</span></span>

### <span data-ttu-id="57d8e-136">Klienta</span><span class="sxs-lookup"><span data-stu-id="57d8e-136">Site</span></span>
<span data-ttu-id="57d8e-137">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="57d8e-137">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="57d8e-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="57d8e-138">OUTPUTS</span></span>

## <span data-ttu-id="57d8e-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="57d8e-139">NOTES</span></span>

## <span data-ttu-id="57d8e-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="57d8e-140">RELATED LINKS</span></span>

