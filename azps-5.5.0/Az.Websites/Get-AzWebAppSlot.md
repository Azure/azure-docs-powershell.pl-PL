---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 100A5980-31E2-41F9-84D4-2F5F0CB78B8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlot.md
ms.openlocfilehash: 4bd0e45df7f1c5c98b61f7f490a59a4c305c2c21
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241554"
---
# <span data-ttu-id="37923-101">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="37923-101">Get-AzWebAppSlot</span></span>

## <span data-ttu-id="37923-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37923-102">SYNOPSIS</span></span>
<span data-ttu-id="37923-103">Otrzymuje miejsce na aplikację Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="37923-103">Gets an Azure Web App slot.</span></span>

## <span data-ttu-id="37923-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="37923-104">SYNTAX</span></span>

### <span data-ttu-id="37923-105">S1</span><span class="sxs-lookup"><span data-stu-id="37923-105">S1</span></span>
```
Get-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="37923-106">S2</span><span class="sxs-lookup"><span data-stu-id="37923-106">S2</span></span>
```
Get-AzWebAppSlot [[-Slot] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="37923-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="37923-107">DESCRIPTION</span></span>
<span data-ttu-id="37923-108">Polecenie **cmdlet Get-AzWebAppSlot** pobiera informacje o gnieździe aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="37923-108">The **Get-AzWebAppSlot** cmdlet gets information about an Azure Web App Slot.</span></span>

## <span data-ttu-id="37923-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="37923-109">EXAMPLES</span></span>

### <span data-ttu-id="37923-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="37923-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -Slot "Slot001"
```

<span data-ttu-id="37923-111">To polecenie pobiera slot o nazwie Slot001 z aplikacji sieci Web o nazwie WebAppStandard, który należy do grupy zasobów Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="37923-111">This command gets the slot named Slot001 from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="37923-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="37923-112">PARAMETERS</span></span>

### <span data-ttu-id="37923-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37923-113">-DefaultProfile</span></span>
<span data-ttu-id="37923-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="37923-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37923-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="37923-115">-Name</span></span>
<span data-ttu-id="37923-116">Nazwa aplikacji WebApp</span><span class="sxs-lookup"><span data-stu-id="37923-116">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37923-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37923-117">-ResourceGroupName</span></span>
<span data-ttu-id="37923-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="37923-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37923-119">— Slot</span><span class="sxs-lookup"><span data-stu-id="37923-119">-Slot</span></span>
<span data-ttu-id="37923-120">Nazwa gniazda aplikacji WebApp</span><span class="sxs-lookup"><span data-stu-id="37923-120">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37923-121">— WebApp</span><span class="sxs-lookup"><span data-stu-id="37923-121">-WebApp</span></span>
<span data-ttu-id="37923-122">Obiekt WebApp</span><span class="sxs-lookup"><span data-stu-id="37923-122">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="37923-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37923-123">CommonParameters</span></span>
<span data-ttu-id="37923-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37923-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37923-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37923-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37923-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="37923-126">INPUTS</span></span>

### <span data-ttu-id="37923-127">System.String</span><span class="sxs-lookup"><span data-stu-id="37923-127">System.String</span></span>

### <span data-ttu-id="37923-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="37923-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="37923-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="37923-129">OUTPUTS</span></span>

### <span data-ttu-id="37923-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="37923-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="37923-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="37923-131">NOTES</span></span>

## <span data-ttu-id="37923-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="37923-132">RELATED LINKS</span></span>

[<span data-ttu-id="37923-133">New-AzWebAppslot</span><span class="sxs-lookup"><span data-stu-id="37923-133">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="37923-134">Remove-AzWebAppslot</span><span class="sxs-lookup"><span data-stu-id="37923-134">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="37923-135">Restart-AzWebAppslot</span><span class="sxs-lookup"><span data-stu-id="37923-135">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="37923-136">Set-AzWebAppslot</span><span class="sxs-lookup"><span data-stu-id="37923-136">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="37923-137">Start-AzWebAppslot</span><span class="sxs-lookup"><span data-stu-id="37923-137">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="37923-138">Stop-AzWebAppslot</span><span class="sxs-lookup"><span data-stu-id="37923-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="37923-139">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="37923-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
