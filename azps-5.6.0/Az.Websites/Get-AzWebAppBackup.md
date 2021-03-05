---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EAAF615B-6139-438B-A2FD-6966E72B3AA9
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackup.md
ms.openlocfilehash: 70dea111b2fc48e2d5063db21dd53a6e9ca76f75
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983802"
---
# <span data-ttu-id="c0353-101">Get-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="c0353-101">Get-AzWebAppBackup</span></span>

## <span data-ttu-id="c0353-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0353-102">SYNOPSIS</span></span>

## <span data-ttu-id="c0353-103">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c0353-103">SYNTAX</span></span>

### <span data-ttu-id="c0353-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="c0353-104">FromResourceName</span></span>
```
Get-AzWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0353-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="c0353-105">FromWebApp</span></span>
```
Get-AzWebAppBackup [-BackupId] <String> [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c0353-106">OPIS</span><span class="sxs-lookup"><span data-stu-id="c0353-106">DESCRIPTION</span></span>
<span data-ttu-id="c0353-107">Polecenie **cmdlet Get-AzWebAppBackup** pobiera określoną kopię zapasową aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="c0353-107">The **Get-AzWebAppBackup** cmdlet gets the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="c0353-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c0353-108">EXAMPLES</span></span>

### <span data-ttu-id="c0353-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c0353-109">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="c0353-110">To polecenie pobiera kopię zapasową o identyfikatorze "12345" z aplikacji Web App o nazwie WebAppStandard, która należy do grupy zasobów Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="c0353-110">This command gets the backup with ID "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="c0353-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c0353-111">PARAMETERS</span></span>

### <span data-ttu-id="c0353-112">- BackupId</span><span class="sxs-lookup"><span data-stu-id="c0353-112">-BackupId</span></span>
<span data-ttu-id="c0353-113">Identyfikator kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="c0353-113">Backup Id</span></span>

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

### <span data-ttu-id="c0353-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0353-114">-DefaultProfile</span></span>
<span data-ttu-id="c0353-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c0353-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0353-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c0353-116">-Name</span></span>
<span data-ttu-id="c0353-117">Nazwa aplikacji WebApp</span><span class="sxs-lookup"><span data-stu-id="c0353-117">Webapp Name</span></span>

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

### <span data-ttu-id="c0353-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0353-118">-ResourceGroupName</span></span>
<span data-ttu-id="c0353-119">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="c0353-119">Resource Group Name</span></span>

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

### <span data-ttu-id="c0353-120">— Slot</span><span class="sxs-lookup"><span data-stu-id="c0353-120">-Slot</span></span>
<span data-ttu-id="c0353-121">Nazwa gniazda</span><span class="sxs-lookup"><span data-stu-id="c0353-121">Slot Name</span></span>

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

### <span data-ttu-id="c0353-122">- WebApp</span><span class="sxs-lookup"><span data-stu-id="c0353-122">-WebApp</span></span>
<span data-ttu-id="c0353-123">Piped WebApp</span><span class="sxs-lookup"><span data-stu-id="c0353-123">Piped WebApp</span></span>

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

### <span data-ttu-id="c0353-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0353-124">CommonParameters</span></span>
<span data-ttu-id="c0353-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0353-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0353-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0353-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0353-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c0353-127">INPUTS</span></span>

### <span data-ttu-id="c0353-128">System.String</span><span class="sxs-lookup"><span data-stu-id="c0353-128">System.String</span></span>

### <span data-ttu-id="c0353-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="c0353-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="c0353-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c0353-130">OUTPUTS</span></span>

### <span data-ttu-id="c0353-131">Microsoft.Azure.Commands.WebApps.Cmdlet.WebApps.AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="c0353-131">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="c0353-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c0353-132">NOTES</span></span>

## <span data-ttu-id="c0353-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c0353-133">RELATED LINKS</span></span>
