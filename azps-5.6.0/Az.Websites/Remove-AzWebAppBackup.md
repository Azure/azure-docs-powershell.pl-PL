---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 65A78654-A490-4B60-8C16-B0CC597EE995
online version: https://docs.microsoft.com/powershell/module/az.websites/remove-azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppBackup.md
ms.openlocfilehash: d6bba1b517f238247291af251d9f510d18029af6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994652"
---
# <span data-ttu-id="8e785-101">Remove-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="8e785-101">Remove-AzWebAppBackup</span></span>

## <span data-ttu-id="8e785-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e785-102">SYNOPSIS</span></span>

## <span data-ttu-id="8e785-103">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8e785-103">SYNTAX</span></span>

### <span data-ttu-id="8e785-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="8e785-104">FromResourceName</span></span>
```
Remove-AzWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e785-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="8e785-105">FromWebApp</span></span>
```
Remove-AzWebAppBackup [-BackupId] <String> [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8e785-106">OPIS</span><span class="sxs-lookup"><span data-stu-id="8e785-106">DESCRIPTION</span></span>
<span data-ttu-id="8e785-107">Polecenie **cmdlet Remove-AzWebAppBackup** usuwa określoną kopię zapasową aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="8e785-107">The **Remove-AzWebAppBackup** cmdlet removes the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="8e785-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8e785-108">EXAMPLES</span></span>

### <span data-ttu-id="8e785-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8e785-109">Example 1</span></span>
```powershell
PS C:\>Remove-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="8e785-110">To polecenie usuwa kopię zapasową z wartością "12345" o identyfikatorze "12345" z aplikacji Sieci Web o nazwie WebAppStandard, która należy do grupy zasobów Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="8e785-110">This command removes the backup with backup with ID of "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="8e785-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e785-111">PARAMETERS</span></span>

### <span data-ttu-id="8e785-112">- BackupId</span><span class="sxs-lookup"><span data-stu-id="8e785-112">-BackupId</span></span>
<span data-ttu-id="8e785-113">Identyfikator kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="8e785-113">Backup Id</span></span>

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

### <span data-ttu-id="8e785-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e785-114">-DefaultProfile</span></span>
<span data-ttu-id="8e785-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8e785-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e785-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8e785-116">-Name</span></span>
<span data-ttu-id="8e785-117">Nazwa aplikacji WebApp</span><span class="sxs-lookup"><span data-stu-id="8e785-117">WebApp Name</span></span>

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

### <span data-ttu-id="8e785-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e785-118">-ResourceGroupName</span></span>
<span data-ttu-id="8e785-119">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="8e785-119">Resource Group Name</span></span>

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

### <span data-ttu-id="8e785-120">— Slot</span><span class="sxs-lookup"><span data-stu-id="8e785-120">-Slot</span></span>
<span data-ttu-id="8e785-121">Nazwa gniazda aplikacji WebApp</span><span class="sxs-lookup"><span data-stu-id="8e785-121">WebApp Slot Name</span></span>

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

### <span data-ttu-id="8e785-122">- WebApp</span><span class="sxs-lookup"><span data-stu-id="8e785-122">-WebApp</span></span>
<span data-ttu-id="8e785-123">Obiekt WebApp</span><span class="sxs-lookup"><span data-stu-id="8e785-123">WebApp Object</span></span>

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

### <span data-ttu-id="8e785-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e785-124">CommonParameters</span></span>
<span data-ttu-id="8e785-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e785-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e785-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e785-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e785-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8e785-127">INPUTS</span></span>

### <span data-ttu-id="8e785-128">System.String</span><span class="sxs-lookup"><span data-stu-id="8e785-128">System.String</span></span>

### <span data-ttu-id="8e785-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="8e785-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="8e785-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8e785-130">OUTPUTS</span></span>

### <span data-ttu-id="8e785-131">Microsoft.Azure.Management.WebSites.Models.BackupItem</span><span class="sxs-lookup"><span data-stu-id="8e785-131">Microsoft.Azure.Management.WebSites.Models.BackupItem</span></span>

## <span data-ttu-id="8e785-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8e785-132">NOTES</span></span>

## <span data-ttu-id="8e785-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8e785-133">RELATED LINKS</span></span>
