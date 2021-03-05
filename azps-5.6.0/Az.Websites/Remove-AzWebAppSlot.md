---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/remove-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSlot.md
ms.openlocfilehash: cca1cc480f529c49f679930d9d88f39f69f6e966
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983786"
---
# <span data-ttu-id="295f6-101">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="295f6-101">Remove-AzWebAppSlot</span></span>

## <span data-ttu-id="295f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="295f6-102">SYNOPSIS</span></span>

## <span data-ttu-id="295f6-103">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="295f6-103">SYNTAX</span></span>

### <span data-ttu-id="295f6-104">S1</span><span class="sxs-lookup"><span data-stu-id="295f6-104">S1</span></span>
```
Remove-AzWebAppSlot [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="295f6-105">S2</span><span class="sxs-lookup"><span data-stu-id="295f6-105">S2</span></span>
```
Remove-AzWebAppSlot [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="295f6-106">OPIS</span><span class="sxs-lookup"><span data-stu-id="295f6-106">DESCRIPTION</span></span>
<span data-ttu-id="295f6-107">Polecenie **cmdlet Remove-AzWebAppSlot** usuwa slot aplikacji Azure Web App pod warunkiem, że nazwa grupy zasobów i aplikacji sieci Web jest podana.</span><span class="sxs-lookup"><span data-stu-id="295f6-107">The **Remove-AzWebAppSlot** cmdlet removes an Azure Web App Slot provided the resource group and Web App name.</span></span>
<span data-ttu-id="295f6-108">To polecenie cmdlet domyślnie usuwa również wszystkie gniazda i metryki.</span><span class="sxs-lookup"><span data-stu-id="295f6-108">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="295f6-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="295f6-109">EXAMPLES</span></span>

### <span data-ttu-id="295f6-110">Przykład 1. Usuwanie gniazda aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="295f6-110">Example 1: Remove a Web App Slot</span></span>
```
PS C:\>Remove-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -Slot "Slot001"
```

<span data-ttu-id="295f6-111">To polecenie usuwa slot o nazwie Slot001 skojarzony z witryną ContosoSite aplikacji Web App należącą do grupy zasobów o nazwie Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="295f6-111">This command removes the Slot named Slot001 associated with Web App ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="295f6-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="295f6-112">PARAMETERS</span></span>

### <span data-ttu-id="295f6-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="295f6-113">-AsJob</span></span>
<span data-ttu-id="295f6-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="295f6-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="295f6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="295f6-115">-DefaultProfile</span></span>
<span data-ttu-id="295f6-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="295f6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="295f6-117">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="295f6-117">-Force</span></span>
<span data-ttu-id="295f6-118">Wymuszanie usuwania opcji</span><span class="sxs-lookup"><span data-stu-id="295f6-118">Forcefully Remove Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="295f6-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="295f6-119">-Name</span></span>
<span data-ttu-id="295f6-120">Nazwa aplikacji WebApp</span><span class="sxs-lookup"><span data-stu-id="295f6-120">WebApp Name</span></span>

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

### <span data-ttu-id="295f6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="295f6-121">-ResourceGroupName</span></span>
<span data-ttu-id="295f6-122">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="295f6-122">Resource Group Name</span></span>

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

### <span data-ttu-id="295f6-123">— Slot</span><span class="sxs-lookup"><span data-stu-id="295f6-123">-Slot</span></span>
<span data-ttu-id="295f6-124">Nazwa gniazda aplikacji WebApp</span><span class="sxs-lookup"><span data-stu-id="295f6-124">WebApp Slot Name</span></span>

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

### <span data-ttu-id="295f6-125">- WebApp</span><span class="sxs-lookup"><span data-stu-id="295f6-125">-WebApp</span></span>
<span data-ttu-id="295f6-126">Obiekt WebApp</span><span class="sxs-lookup"><span data-stu-id="295f6-126">WebApp Object</span></span>

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

### <span data-ttu-id="295f6-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="295f6-127">-Confirm</span></span>
<span data-ttu-id="295f6-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="295f6-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="295f6-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="295f6-129">-WhatIf</span></span>
<span data-ttu-id="295f6-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="295f6-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="295f6-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="295f6-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="295f6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="295f6-132">CommonParameters</span></span>
<span data-ttu-id="295f6-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="295f6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="295f6-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="295f6-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="295f6-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="295f6-135">INPUTS</span></span>

### <span data-ttu-id="295f6-136">System.String</span><span class="sxs-lookup"><span data-stu-id="295f6-136">System.String</span></span>

### <span data-ttu-id="295f6-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="295f6-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="295f6-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="295f6-138">OUTPUTS</span></span>

### <span data-ttu-id="295f6-139">Microsoft.Azure.AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="295f6-139">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="295f6-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="295f6-140">NOTES</span></span>

## <span data-ttu-id="295f6-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="295f6-141">RELATED LINKS</span></span>

[<span data-ttu-id="295f6-142">Get-AzWebAppslot</span><span class="sxs-lookup"><span data-stu-id="295f6-142">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="295f6-143">New-AzWebAppslot</span><span class="sxs-lookup"><span data-stu-id="295f6-143">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="295f6-144">Restart-AzWebAppslot</span><span class="sxs-lookup"><span data-stu-id="295f6-144">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="295f6-145">Set-AzWebAppslot</span><span class="sxs-lookup"><span data-stu-id="295f6-145">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="295f6-146">Start-AzWebAppslot</span><span class="sxs-lookup"><span data-stu-id="295f6-146">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="295f6-147">Stop-AzWebAppslot</span><span class="sxs-lookup"><span data-stu-id="295f6-147">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="295f6-148">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="295f6-148">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
