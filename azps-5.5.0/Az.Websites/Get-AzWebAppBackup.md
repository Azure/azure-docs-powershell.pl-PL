---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EAAF615B-6139-438B-A2FD-6966E72B3AA9
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackup.md
ms.openlocfilehash: e8c3f7543062613527e7f52be2cd6493f53c5f60
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188715"
---
# <span data-ttu-id="ae54b-101">Get-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="ae54b-101">Get-AzWebAppBackup</span></span>

## <span data-ttu-id="ae54b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae54b-102">SYNOPSIS</span></span>

## <span data-ttu-id="ae54b-103">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ae54b-103">SYNTAX</span></span>

### <span data-ttu-id="ae54b-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="ae54b-104">FromResourceName</span></span>
```
Get-AzWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae54b-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="ae54b-105">FromWebApp</span></span>
```
Get-AzWebAppBackup [-BackupId] <String> [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ae54b-106">OPIS</span><span class="sxs-lookup"><span data-stu-id="ae54b-106">DESCRIPTION</span></span>
<span data-ttu-id="ae54b-107">Polecenie **cmdlet Get-AzWebAppBackup** pobiera określoną kopię zapasową aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="ae54b-107">The **Get-AzWebAppBackup** cmdlet gets the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="ae54b-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ae54b-108">EXAMPLES</span></span>

### <span data-ttu-id="ae54b-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ae54b-109">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="ae54b-110">To polecenie pobiera kopię zapasową o identyfikatorze "12345" z aplikacji Web App o nazwie WebAppStandard, która należy do grupy zasobów Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="ae54b-110">This command gets the backup with ID "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="ae54b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ae54b-111">PARAMETERS</span></span>

### <span data-ttu-id="ae54b-112">- BackupId</span><span class="sxs-lookup"><span data-stu-id="ae54b-112">-BackupId</span></span>
<span data-ttu-id="ae54b-113">Identyfikator kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="ae54b-113">Backup Id</span></span>

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

### <span data-ttu-id="ae54b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae54b-114">-DefaultProfile</span></span>
<span data-ttu-id="ae54b-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ae54b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae54b-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ae54b-116">-Name</span></span>
<span data-ttu-id="ae54b-117">Nazwa aplikacji WebApp</span><span class="sxs-lookup"><span data-stu-id="ae54b-117">Webapp Name</span></span>

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

### <span data-ttu-id="ae54b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae54b-118">-ResourceGroupName</span></span>
<span data-ttu-id="ae54b-119">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="ae54b-119">Resource Group Name</span></span>

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

### <span data-ttu-id="ae54b-120">— Slot</span><span class="sxs-lookup"><span data-stu-id="ae54b-120">-Slot</span></span>
<span data-ttu-id="ae54b-121">Nazwa gniazda</span><span class="sxs-lookup"><span data-stu-id="ae54b-121">Slot Name</span></span>

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

### <span data-ttu-id="ae54b-122">- WebApp</span><span class="sxs-lookup"><span data-stu-id="ae54b-122">-WebApp</span></span>
<span data-ttu-id="ae54b-123">Piped WebApp</span><span class="sxs-lookup"><span data-stu-id="ae54b-123">Piped WebApp</span></span>

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

### <span data-ttu-id="ae54b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae54b-124">CommonParameters</span></span>
<span data-ttu-id="ae54b-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae54b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae54b-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae54b-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae54b-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ae54b-127">INPUTS</span></span>

### <span data-ttu-id="ae54b-128">System.String</span><span class="sxs-lookup"><span data-stu-id="ae54b-128">System.String</span></span>

### <span data-ttu-id="ae54b-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="ae54b-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="ae54b-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ae54b-130">OUTPUTS</span></span>

### <span data-ttu-id="ae54b-131">Microsoft.Azure.Commands.WebApps.Cmdlet.WebApps.AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="ae54b-131">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="ae54b-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ae54b-132">NOTES</span></span>

## <span data-ttu-id="ae54b-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ae54b-133">RELATED LINKS</span></span>
