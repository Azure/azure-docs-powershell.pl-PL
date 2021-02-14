---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 0FDDDEE1-CEAD-46DA-A7EB-EE477ED59749
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/start-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebAppSlot.md
ms.openlocfilehash: 4425c344fb0c9e0e3441c172915be11002ee8b1b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241499"
---
# <span data-ttu-id="8b93f-101">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8b93f-101">Start-AzWebAppSlot</span></span>

## <span data-ttu-id="8b93f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b93f-102">SYNOPSIS</span></span>
<span data-ttu-id="8b93f-103">Pozwala na rozpoczęcie pracy w miejscu aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="8b93f-103">Starts an Azure Web App slot.</span></span>

## <span data-ttu-id="8b93f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8b93f-104">SYNTAX</span></span>

### <span data-ttu-id="8b93f-105">S1</span><span class="sxs-lookup"><span data-stu-id="8b93f-105">S1</span></span>
```
Start-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b93f-106">S2</span><span class="sxs-lookup"><span data-stu-id="8b93f-106">S2</span></span>
```
Start-AzWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b93f-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="8b93f-107">DESCRIPTION</span></span>
<span data-ttu-id="8b93f-108">Polecenie **cmdlet Start-AzWebAppSlot** uruchamia slot aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="8b93f-108">The **Start-AzWebAppSlot** cmdlet starts an Azure Web App Slot.</span></span>

## <span data-ttu-id="8b93f-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8b93f-109">EXAMPLES</span></span>

### <span data-ttu-id="8b93f-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8b93f-110">Example 1</span></span>
```
PS C:\>Start-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="8b93f-111">To polecenie uruchamia slot o nazwie Slot001 dotyczący aplikacji sieci Web o nazwie ContosoWebApp, która należy do grupy zasobów o nazwie Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="8b93f-111">This command starts the Slot named Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="8b93f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8b93f-112">PARAMETERS</span></span>

### <span data-ttu-id="8b93f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b93f-113">-DefaultProfile</span></span>
<span data-ttu-id="8b93f-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8b93f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b93f-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8b93f-115">-Name</span></span>
<span data-ttu-id="8b93f-116">Nazwa aplikacji WebApp</span><span class="sxs-lookup"><span data-stu-id="8b93f-116">WebApp Name</span></span>

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

### <span data-ttu-id="8b93f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b93f-117">-ResourceGroupName</span></span>
<span data-ttu-id="8b93f-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="8b93f-118">Resource Group Name</span></span>

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

### <span data-ttu-id="8b93f-119">— Slot</span><span class="sxs-lookup"><span data-stu-id="8b93f-119">-Slot</span></span>
<span data-ttu-id="8b93f-120">Nazwa gniazda aplikacji WebApp</span><span class="sxs-lookup"><span data-stu-id="8b93f-120">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b93f-121">— WebApp</span><span class="sxs-lookup"><span data-stu-id="8b93f-121">-WebApp</span></span>
<span data-ttu-id="8b93f-122">Obiekt WebApp</span><span class="sxs-lookup"><span data-stu-id="8b93f-122">WebApp Object</span></span>

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

### <span data-ttu-id="8b93f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b93f-123">CommonParameters</span></span>
<span data-ttu-id="8b93f-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b93f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b93f-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b93f-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b93f-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8b93f-126">INPUTS</span></span>

### <span data-ttu-id="8b93f-127">System.String</span><span class="sxs-lookup"><span data-stu-id="8b93f-127">System.String</span></span>

### <span data-ttu-id="8b93f-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="8b93f-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="8b93f-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8b93f-129">OUTPUTS</span></span>

### <span data-ttu-id="8b93f-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="8b93f-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="8b93f-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8b93f-131">NOTES</span></span>

## <span data-ttu-id="8b93f-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8b93f-132">RELATED LINKS</span></span>

[<span data-ttu-id="8b93f-133">Get-AzWebAppslot</span><span class="sxs-lookup"><span data-stu-id="8b93f-133">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="8b93f-134">New-AzWebAppslot</span><span class="sxs-lookup"><span data-stu-id="8b93f-134">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="8b93f-135">Remove-AzWebAppslot</span><span class="sxs-lookup"><span data-stu-id="8b93f-135">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="8b93f-136">Restart-AzWebAppslot</span><span class="sxs-lookup"><span data-stu-id="8b93f-136">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="8b93f-137">Set-AzWebAppslot</span><span class="sxs-lookup"><span data-stu-id="8b93f-137">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="8b93f-138">Stop-AzWebAppslot</span><span class="sxs-lookup"><span data-stu-id="8b93f-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="8b93f-139">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8b93f-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
