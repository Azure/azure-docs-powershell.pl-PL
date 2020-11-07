---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: D3FE0440-C663-4379-8F5F-2E66EF024E5D
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/new-Azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/New-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/New-AzWebAppBackup.md
ms.openlocfilehash: a01c49ac6591cfec7d8087d664ba61ddd825ac5e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891905"
---
# <span data-ttu-id="20d91-101">New-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="20d91-101">New-AzWebAppBackup</span></span>

## <span data-ttu-id="20d91-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="20d91-102">SYNOPSIS</span></span>

## <span data-ttu-id="20d91-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="20d91-103">SYNTAX</span></span>

### <span data-ttu-id="20d91-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="20d91-104">FromResourceName</span></span>
```
New-AzWebAppBackup [[-BackupName] <String>] [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="20d91-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="20d91-105">FromWebApp</span></span>
```
New-AzWebAppBackup [[-BackupName] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="20d91-106">Opis</span><span class="sxs-lookup"><span data-stu-id="20d91-106">DESCRIPTION</span></span>
<span data-ttu-id="20d91-107">Polecenie cmdlet **New-AzWebAppBackup** tworzy kopię zapasową aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="20d91-107">The **New-AzWebAppBackup** cmdlet creates an Azure Web App Backup.</span></span>

## <span data-ttu-id="20d91-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="20d91-108">EXAMPLES</span></span>

### <span data-ttu-id="20d91-109">1:1</span><span class="sxs-lookup"><span data-stu-id="20d91-109">1:</span></span>
```
PS C:\> New-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net"
```

<span data-ttu-id="20d91-110">Tworzy kopię zapasową określonego ContosoWebApp aplikacji, który znajduje się w obszarze domyślne grupy zasobów — w sieci Web — zachód. https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="20d91-110">Creates a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="20d91-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="20d91-111">PARAMETERS</span></span>

### <span data-ttu-id="20d91-112">-Backupname</span><span class="sxs-lookup"><span data-stu-id="20d91-112">-BackupName</span></span>
<span data-ttu-id="20d91-113">Nazwa kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="20d91-113">Backup Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20d91-114">-Bazy danych</span><span class="sxs-lookup"><span data-stu-id="20d91-114">-Databases</span></span>
<span data-ttu-id="20d91-115">Bazy danych typu DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="20d91-115">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="20d91-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20d91-116">-DefaultProfile</span></span>
<span data-ttu-id="20d91-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="20d91-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20d91-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="20d91-118">-Name</span></span>
<span data-ttu-id="20d91-119">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="20d91-119">WebApp Name</span></span>

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

### <span data-ttu-id="20d91-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20d91-120">-ResourceGroupName</span></span>
<span data-ttu-id="20d91-121">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="20d91-121">Resource Group Name</span></span>

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

### <span data-ttu-id="20d91-122">-Slot</span><span class="sxs-lookup"><span data-stu-id="20d91-122">-Slot</span></span>
<span data-ttu-id="20d91-123">Nazwa gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="20d91-123">WebApp Slot Name</span></span>

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

### <span data-ttu-id="20d91-124">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="20d91-124">-StorageAccountUrl</span></span>
<span data-ttu-id="20d91-125">Adres URL konta magazynu</span><span class="sxs-lookup"><span data-stu-id="20d91-125">Storage Account Url</span></span>

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

### <span data-ttu-id="20d91-126">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="20d91-126">-WebApp</span></span>
<span data-ttu-id="20d91-127">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="20d91-127">WebApp Object</span></span>

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

### <span data-ttu-id="20d91-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20d91-128">CommonParameters</span></span>
<span data-ttu-id="20d91-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20d91-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20d91-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20d91-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20d91-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="20d91-131">INPUTS</span></span>

### <span data-ttu-id="20d91-132">Klienta</span><span class="sxs-lookup"><span data-stu-id="20d91-132">Site</span></span>
<span data-ttu-id="20d91-133">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="20d91-133">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="20d91-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="20d91-134">OUTPUTS</span></span>

### <span data-ttu-id="20d91-135">Microsoft. Azure. polecenia. webapps. polecenia cmdlet. webapps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="20d91-135">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="20d91-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="20d91-136">NOTES</span></span>

## <span data-ttu-id="20d91-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="20d91-137">RELATED LINKS</span></span>

