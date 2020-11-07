---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D3FE0440-C663-4379-8F5F-2E66EF024E5D
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppBackup.md
ms.openlocfilehash: 2ef015c3f793dd4636632f17568feb9aaf1b5ad2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707299"
---
# <span data-ttu-id="944b3-101">New-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="944b3-101">New-AzWebAppBackup</span></span>

## <span data-ttu-id="944b3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="944b3-102">SYNOPSIS</span></span>

## <span data-ttu-id="944b3-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="944b3-103">SYNTAX</span></span>

### <span data-ttu-id="944b3-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="944b3-104">FromResourceName</span></span>
```
New-AzWebAppBackup [[-BackupName] <String>] [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="944b3-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="944b3-105">FromWebApp</span></span>
```
New-AzWebAppBackup [[-BackupName] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="944b3-106">Opis</span><span class="sxs-lookup"><span data-stu-id="944b3-106">DESCRIPTION</span></span>
<span data-ttu-id="944b3-107">Polecenie cmdlet **New-AzWebAppBackup** tworzy kopię zapasową aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="944b3-107">The **New-AzWebAppBackup** cmdlet creates an Azure Web App Backup.</span></span>

## <span data-ttu-id="944b3-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="944b3-108">EXAMPLES</span></span>

### <span data-ttu-id="944b3-109">1:1</span><span class="sxs-lookup"><span data-stu-id="944b3-109">1:</span></span>
```
PS C:\> New-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net"
```

<span data-ttu-id="944b3-110">Tworzy kopię zapasową określonego ContosoWebApp aplikacji, który znajduje się w obszarze domyślne grupy zasobów — w sieci Web — zachód. https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="944b3-110">Creates a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="944b3-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="944b3-111">PARAMETERS</span></span>

### <span data-ttu-id="944b3-112">-Backupname</span><span class="sxs-lookup"><span data-stu-id="944b3-112">-BackupName</span></span>
<span data-ttu-id="944b3-113">Nazwa kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="944b3-113">Backup Name</span></span>

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

### <span data-ttu-id="944b3-114">-Bazy danych</span><span class="sxs-lookup"><span data-stu-id="944b3-114">-Databases</span></span>
<span data-ttu-id="944b3-115">Bazy danych typu DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="944b3-115">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="944b3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="944b3-116">-DefaultProfile</span></span>
<span data-ttu-id="944b3-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="944b3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="944b3-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="944b3-118">-Name</span></span>
<span data-ttu-id="944b3-119">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="944b3-119">WebApp Name</span></span>

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

### <span data-ttu-id="944b3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="944b3-120">-ResourceGroupName</span></span>
<span data-ttu-id="944b3-121">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="944b3-121">Resource Group Name</span></span>

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

### <span data-ttu-id="944b3-122">-Slot</span><span class="sxs-lookup"><span data-stu-id="944b3-122">-Slot</span></span>
<span data-ttu-id="944b3-123">Nazwa gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="944b3-123">WebApp Slot Name</span></span>

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

### <span data-ttu-id="944b3-124">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="944b3-124">-StorageAccountUrl</span></span>
<span data-ttu-id="944b3-125">Adres URL konta magazynu</span><span class="sxs-lookup"><span data-stu-id="944b3-125">Storage Account Url</span></span>

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

### <span data-ttu-id="944b3-126">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="944b3-126">-WebApp</span></span>
<span data-ttu-id="944b3-127">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="944b3-127">WebApp Object</span></span>

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

### <span data-ttu-id="944b3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="944b3-128">CommonParameters</span></span>
<span data-ttu-id="944b3-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="944b3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="944b3-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="944b3-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="944b3-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="944b3-131">INPUTS</span></span>

### <span data-ttu-id="944b3-132">System. String</span><span class="sxs-lookup"><span data-stu-id="944b3-132">System.String</span></span>

### <span data-ttu-id="944b3-133">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="944b3-133">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

### <span data-ttu-id="944b3-134">Microsoft. Azure. Management. Web. MODELES. DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="944b3-134">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]</span></span>

## <span data-ttu-id="944b3-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="944b3-135">OUTPUTS</span></span>

### <span data-ttu-id="944b3-136">Microsoft. Azure. polecenia. webapps. polecenia cmdlet. webapps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="944b3-136">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="944b3-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="944b3-137">NOTES</span></span>

## <span data-ttu-id="944b3-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="944b3-138">RELATED LINKS</span></span>
