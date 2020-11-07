---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: D3FE0440-C663-4379-8F5F-2E66EF024E5D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappbackup
schema: 2.0.0
ms.openlocfilehash: 7245697cab6184aa5fc2f7c292875f96cf3de3fb
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898122"
---
# <span data-ttu-id="28ec6-101">New-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="28ec6-101">New-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="28ec6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="28ec6-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28ec6-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="28ec6-103">SYNTAX</span></span>

### <span data-ttu-id="28ec6-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="28ec6-104">FromResourceName</span></span>
```
New-AzureRmWebAppBackup [[-BackupName] <String>] [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="28ec6-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="28ec6-105">FromWebApp</span></span>
```
New-AzureRmWebAppBackup [[-BackupName] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="28ec6-106">Opis</span><span class="sxs-lookup"><span data-stu-id="28ec6-106">DESCRIPTION</span></span>
<span data-ttu-id="28ec6-107">Polecenie cmdlet **New-AzureRmWebAppBackup** tworzy kopię zapasową aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="28ec6-107">The **New-AzureRmWebAppBackup** cmdlet creates an Azure Web App Backup.</span></span>

## <span data-ttu-id="28ec6-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="28ec6-108">EXAMPLES</span></span>

### <span data-ttu-id="28ec6-109">1:1</span><span class="sxs-lookup"><span data-stu-id="28ec6-109">1:</span></span>
```
PS C:\> New-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net"
```

<span data-ttu-id="28ec6-110">Tworzy kopię zapasową określonego ContosoWebApp aplikacji, który znajduje się w obszarze domyślne grupy zasobów — w sieci Web — zachód. https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="28ec6-110">Creates a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="28ec6-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="28ec6-111">PARAMETERS</span></span>

### <span data-ttu-id="28ec6-112">-Backupname</span><span class="sxs-lookup"><span data-stu-id="28ec6-112">-BackupName</span></span>
<span data-ttu-id="28ec6-113">Nazwa kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="28ec6-113">Backup Name</span></span>

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

### <span data-ttu-id="28ec6-114">-Bazy danych</span><span class="sxs-lookup"><span data-stu-id="28ec6-114">-Databases</span></span>
<span data-ttu-id="28ec6-115">Bazy danych typu DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="28ec6-115">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="28ec6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28ec6-116">-DefaultProfile</span></span>
<span data-ttu-id="28ec6-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="28ec6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28ec6-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="28ec6-118">-Name</span></span>
<span data-ttu-id="28ec6-119">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="28ec6-119">WebApp Name</span></span>

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

### <span data-ttu-id="28ec6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28ec6-120">-ResourceGroupName</span></span>
<span data-ttu-id="28ec6-121">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="28ec6-121">Resource Group Name</span></span>

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

### <span data-ttu-id="28ec6-122">-Slot</span><span class="sxs-lookup"><span data-stu-id="28ec6-122">-Slot</span></span>
<span data-ttu-id="28ec6-123">Nazwa gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="28ec6-123">WebApp Slot Name</span></span>

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

### <span data-ttu-id="28ec6-124">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="28ec6-124">-StorageAccountUrl</span></span>
<span data-ttu-id="28ec6-125">Adres URL konta magazynu</span><span class="sxs-lookup"><span data-stu-id="28ec6-125">Storage Account Url</span></span>

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

### <span data-ttu-id="28ec6-126">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="28ec6-126">-WebApp</span></span>
<span data-ttu-id="28ec6-127">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="28ec6-127">WebApp Object</span></span>

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

### <span data-ttu-id="28ec6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28ec6-128">CommonParameters</span></span>
<span data-ttu-id="28ec6-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28ec6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28ec6-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28ec6-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28ec6-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="28ec6-131">INPUTS</span></span>

### <span data-ttu-id="28ec6-132">Klienta</span><span class="sxs-lookup"><span data-stu-id="28ec6-132">Site</span></span>
<span data-ttu-id="28ec6-133">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="28ec6-133">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="28ec6-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="28ec6-134">OUTPUTS</span></span>

### <span data-ttu-id="28ec6-135">Microsoft. Azure. polecenia. webapps. polecenia cmdlet. webapps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="28ec6-135">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="28ec6-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="28ec6-136">NOTES</span></span>

## <span data-ttu-id="28ec6-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="28ec6-137">RELATED LINKS</span></span>

