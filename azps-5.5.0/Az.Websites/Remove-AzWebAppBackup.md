---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 65A78654-A490-4B60-8C16-B0CC597EE995
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppBackup.md
ms.openlocfilehash: e50c711e730f3af79ce5d8825e6beeee9b663e00
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182442"
---
# <span data-ttu-id="8148f-101">Remove-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="8148f-101">Remove-AzWebAppBackup</span></span>

## <span data-ttu-id="8148f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8148f-102">SYNOPSIS</span></span>

## <span data-ttu-id="8148f-103">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8148f-103">SYNTAX</span></span>

### <span data-ttu-id="8148f-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="8148f-104">FromResourceName</span></span>
```
Remove-AzWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8148f-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="8148f-105">FromWebApp</span></span>
```
Remove-AzWebAppBackup [-BackupId] <String> [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8148f-106">OPIS</span><span class="sxs-lookup"><span data-stu-id="8148f-106">DESCRIPTION</span></span>
<span data-ttu-id="8148f-107">Polecenie **cmdlet Remove-AzWebAppBackup** usuwa określoną kopię zapasową aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="8148f-107">The **Remove-AzWebAppBackup** cmdlet removes the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="8148f-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8148f-108">EXAMPLES</span></span>

### <span data-ttu-id="8148f-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8148f-109">Example 1</span></span>
```powershell
PS C:\>Remove-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="8148f-110">To polecenie usuwa kopię zapasową z wartością "12345" o identyfikatorze "12345" z aplikacji Sieci Web o nazwie WebAppStandard, która należy do grupy zasobów Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="8148f-110">This command removes the backup with backup with ID of "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="8148f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8148f-111">PARAMETERS</span></span>

### <span data-ttu-id="8148f-112">- BackupId</span><span class="sxs-lookup"><span data-stu-id="8148f-112">-BackupId</span></span>
<span data-ttu-id="8148f-113">Identyfikator kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="8148f-113">Backup Id</span></span>

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

### <span data-ttu-id="8148f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8148f-114">-DefaultProfile</span></span>
<span data-ttu-id="8148f-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8148f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8148f-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8148f-116">-Name</span></span>
<span data-ttu-id="8148f-117">Nazwa aplikacji WebApp</span><span class="sxs-lookup"><span data-stu-id="8148f-117">WebApp Name</span></span>

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

### <span data-ttu-id="8148f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8148f-118">-ResourceGroupName</span></span>
<span data-ttu-id="8148f-119">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="8148f-119">Resource Group Name</span></span>

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

### <span data-ttu-id="8148f-120">— Slot</span><span class="sxs-lookup"><span data-stu-id="8148f-120">-Slot</span></span>
<span data-ttu-id="8148f-121">Nazwa gniazda aplikacji WebApp</span><span class="sxs-lookup"><span data-stu-id="8148f-121">WebApp Slot Name</span></span>

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

### <span data-ttu-id="8148f-122">— WebApp</span><span class="sxs-lookup"><span data-stu-id="8148f-122">-WebApp</span></span>
<span data-ttu-id="8148f-123">Obiekt WebApp</span><span class="sxs-lookup"><span data-stu-id="8148f-123">WebApp Object</span></span>

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

### <span data-ttu-id="8148f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8148f-124">CommonParameters</span></span>
<span data-ttu-id="8148f-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8148f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8148f-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8148f-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8148f-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8148f-127">INPUTS</span></span>

### <span data-ttu-id="8148f-128">System.String</span><span class="sxs-lookup"><span data-stu-id="8148f-128">System.String</span></span>

### <span data-ttu-id="8148f-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="8148f-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="8148f-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8148f-130">OUTPUTS</span></span>

### <span data-ttu-id="8148f-131">Microsoft.Azure.Management.WebSites.Models.BackupItem</span><span class="sxs-lookup"><span data-stu-id="8148f-131">Microsoft.Azure.Management.WebSites.Models.BackupItem</span></span>

## <span data-ttu-id="8148f-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8148f-132">NOTES</span></span>

## <span data-ttu-id="8148f-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8148f-133">RELATED LINKS</span></span>
