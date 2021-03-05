---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 9057185C-6F22-4C4A-8480-BE542B5D6BAF
online version: https://docs.microsoft.com/powershell/module/az.websites/remove-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebApp.md
ms.openlocfilehash: 1ce172ea2f1851f2f75a95a3037798ca3b3a2bf4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961066"
---
# <span data-ttu-id="41349-101">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="41349-101">Remove-AzWebApp</span></span>

## <span data-ttu-id="41349-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41349-102">SYNOPSIS</span></span>
<span data-ttu-id="41349-103">Usuwa aplikację Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="41349-103">Removes an Azure Web App.</span></span>

## <span data-ttu-id="41349-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="41349-104">SYNTAX</span></span>

### <span data-ttu-id="41349-105">S1</span><span class="sxs-lookup"><span data-stu-id="41349-105">S1</span></span>
```
Remove-AzWebApp [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41349-106">S2</span><span class="sxs-lookup"><span data-stu-id="41349-106">S2</span></span>
```
Remove-AzWebApp [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41349-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="41349-107">DESCRIPTION</span></span>
<span data-ttu-id="41349-108">Polecenie **cmdlet Remove-AzWebApp** usuwa aplikację Azure Web App podaną nazwę grupy zasobów i aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="41349-108">The **Remove-AzWebApp** cmdlet removes an Azure Web App provided the resource group and Web App name.</span></span>
<span data-ttu-id="41349-109">To polecenie cmdlet domyślnie usuwa również wszystkie gniazda i metryki.</span><span class="sxs-lookup"><span data-stu-id="41349-109">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="41349-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="41349-110">EXAMPLES</span></span>

### <span data-ttu-id="41349-111">Przykład 1. Usuwanie aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="41349-111">Example 1: Remove a Web App</span></span>
```
PS C:\>Remove-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="41349-112">To polecenie usuwa aplikację Azure Web App o nazwie ContosoSite należącą do grupy zasobów o nazwie Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="41349-112">This command removes the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="41349-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="41349-113">PARAMETERS</span></span>

### <span data-ttu-id="41349-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="41349-114">-AsJob</span></span>
<span data-ttu-id="41349-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="41349-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="41349-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41349-116">-DefaultProfile</span></span>
<span data-ttu-id="41349-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="41349-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41349-118">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="41349-118">-Force</span></span>
<span data-ttu-id="41349-119">Wymuszanie usuwania opcji</span><span class="sxs-lookup"><span data-stu-id="41349-119">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="41349-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="41349-120">-Name</span></span>
<span data-ttu-id="41349-121">Nazwa aplikacji WebApp</span><span class="sxs-lookup"><span data-stu-id="41349-121">WebApp Name</span></span>

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

### <span data-ttu-id="41349-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41349-122">-ResourceGroupName</span></span>
<span data-ttu-id="41349-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="41349-123">Resource Group Name</span></span>

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

### <span data-ttu-id="41349-124">- WebApp</span><span class="sxs-lookup"><span data-stu-id="41349-124">-WebApp</span></span>
<span data-ttu-id="41349-125">Obiekt WebApp</span><span class="sxs-lookup"><span data-stu-id="41349-125">WebApp Object</span></span>

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

### <span data-ttu-id="41349-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="41349-126">-Confirm</span></span>
<span data-ttu-id="41349-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie. Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="41349-127">Prompts you for confirmation before running the cmdlet.Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41349-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41349-128">-WhatIf</span></span>
<span data-ttu-id="41349-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41349-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41349-130">Polecenie cmdlet nie zostanie uruchomione. Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41349-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41349-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="41349-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41349-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41349-132">CommonParameters</span></span>
<span data-ttu-id="41349-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41349-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41349-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41349-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41349-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="41349-135">INPUTS</span></span>

### <span data-ttu-id="41349-136">System.String</span><span class="sxs-lookup"><span data-stu-id="41349-136">System.String</span></span>

### <span data-ttu-id="41349-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="41349-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="41349-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="41349-138">OUTPUTS</span></span>

### <span data-ttu-id="41349-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="41349-139">System.Void</span></span>

## <span data-ttu-id="41349-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="41349-140">NOTES</span></span>

## <span data-ttu-id="41349-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="41349-141">RELATED LINKS</span></span>

[<span data-ttu-id="41349-142">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="41349-142">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="41349-143">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="41349-143">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="41349-144">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="41349-144">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="41349-145">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="41349-145">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="41349-146">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="41349-146">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


