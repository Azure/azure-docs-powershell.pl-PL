---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: D3FE0440-C663-4379-8F5F-2E66EF024E5D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppBackup.md
ms.openlocfilehash: 03c9b54dd83f4689f763ef45e0f9a7c0d8b89672
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719217"
---
# <span data-ttu-id="1484a-101">New-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="1484a-101">New-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="1484a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1484a-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1484a-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1484a-103">SYNTAX</span></span>

### <span data-ttu-id="1484a-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="1484a-104">FromResourceName</span></span>
```
New-AzureRmWebAppBackup [[-BackupName] <String>] [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="1484a-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="1484a-105">FromWebApp</span></span>
```
New-AzureRmWebAppBackup [[-BackupName] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="1484a-106">Opis</span><span class="sxs-lookup"><span data-stu-id="1484a-106">DESCRIPTION</span></span>
<span data-ttu-id="1484a-107">Polecenie cmdlet **New-AzureRmWebAppBackup** tworzy kopię zapasową aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="1484a-107">The **New-AzureRmWebAppBackup** cmdlet creates an Azure Web App Backup.</span></span>

## <span data-ttu-id="1484a-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1484a-108">EXAMPLES</span></span>

### <span data-ttu-id="1484a-109">1:1</span><span class="sxs-lookup"><span data-stu-id="1484a-109">1:</span></span>
```
PS C:\> New-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net"
```

<span data-ttu-id="1484a-110">Tworzy kopię zapasową określonego ContosoWebApp aplikacji, który znajduje się w obszarze domyślne grupy zasobów — w sieci Web — zachód. https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="1484a-110">Creates a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="1484a-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1484a-111">PARAMETERS</span></span>

### <span data-ttu-id="1484a-112">-Backupname</span><span class="sxs-lookup"><span data-stu-id="1484a-112">-BackupName</span></span>
<span data-ttu-id="1484a-113">Nazwa kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="1484a-113">Backup Name</span></span>

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

### <span data-ttu-id="1484a-114">-Bazy danych</span><span class="sxs-lookup"><span data-stu-id="1484a-114">-Databases</span></span>
<span data-ttu-id="1484a-115">Bazy danych typu DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="1484a-115">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="1484a-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1484a-116">-Name</span></span>
<span data-ttu-id="1484a-117">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="1484a-117">WebApp Name</span></span>

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

### <span data-ttu-id="1484a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1484a-118">-ResourceGroupName</span></span>
<span data-ttu-id="1484a-119">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="1484a-119">Resource Group Name</span></span>

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

### <span data-ttu-id="1484a-120">-Slot</span><span class="sxs-lookup"><span data-stu-id="1484a-120">-Slot</span></span>
<span data-ttu-id="1484a-121">Nazwa gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="1484a-121">WebApp Slot Name</span></span>

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

### <span data-ttu-id="1484a-122">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="1484a-122">-StorageAccountUrl</span></span>
<span data-ttu-id="1484a-123">Adres URL konta magazynu</span><span class="sxs-lookup"><span data-stu-id="1484a-123">Storage Account Url</span></span>

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

### <span data-ttu-id="1484a-124">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="1484a-124">-WebApp</span></span>
<span data-ttu-id="1484a-125">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="1484a-125">WebApp Object</span></span>

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

### <span data-ttu-id="1484a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1484a-126">-DefaultProfile</span></span>
<span data-ttu-id="1484a-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1484a-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1484a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1484a-128">CommonParameters</span></span>
<span data-ttu-id="1484a-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1484a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1484a-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1484a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1484a-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1484a-131">INPUTS</span></span>

### <span data-ttu-id="1484a-132">Klienta</span><span class="sxs-lookup"><span data-stu-id="1484a-132">Site</span></span>
<span data-ttu-id="1484a-133">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="1484a-133">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="1484a-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1484a-134">OUTPUTS</span></span>

### <span data-ttu-id="1484a-135">Microsoft. Azure. polecenia. webapps. polecenia cmdlet. webapps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="1484a-135">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="1484a-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1484a-136">NOTES</span></span>

## <span data-ttu-id="1484a-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1484a-137">RELATED LINKS</span></span>

