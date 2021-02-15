---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 9057185C-6F22-4C4A-8480-BE542B5D6BAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebApp.md
ms.openlocfilehash: 64d463e6cbe3012b8d49e0a61b4f081f286e25b5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182443"
---
# <span data-ttu-id="b52e9-101">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b52e9-101">Remove-AzWebApp</span></span>

## <span data-ttu-id="b52e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b52e9-102">SYNOPSIS</span></span>
<span data-ttu-id="b52e9-103">Usuwa aplikację Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="b52e9-103">Removes an Azure Web App.</span></span>

## <span data-ttu-id="b52e9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b52e9-104">SYNTAX</span></span>

### <span data-ttu-id="b52e9-105">S1</span><span class="sxs-lookup"><span data-stu-id="b52e9-105">S1</span></span>
```
Remove-AzWebApp [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b52e9-106">S2</span><span class="sxs-lookup"><span data-stu-id="b52e9-106">S2</span></span>
```
Remove-AzWebApp [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b52e9-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="b52e9-107">DESCRIPTION</span></span>
<span data-ttu-id="b52e9-108">Polecenie **cmdlet Remove-AzWebApp** usuwa aplikację Azure Web App pod warunkiem, że grupa zasobów i nazwa aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="b52e9-108">The **Remove-AzWebApp** cmdlet removes an Azure Web App provided the resource group and Web App name.</span></span>
<span data-ttu-id="b52e9-109">To polecenie cmdlet domyślnie usuwa również wszystkie gniazda i metryki.</span><span class="sxs-lookup"><span data-stu-id="b52e9-109">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="b52e9-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b52e9-110">EXAMPLES</span></span>

### <span data-ttu-id="b52e9-111">Przykład 1. Usuwanie aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="b52e9-111">Example 1: Remove a Web App</span></span>
```
PS C:\>Remove-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="b52e9-112">To polecenie usuwa aplikację Azure Web App o nazwie ContosoSite należącą do grupy zasobów o nazwie Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="b52e9-112">This command removes the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="b52e9-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b52e9-113">PARAMETERS</span></span>

### <span data-ttu-id="b52e9-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="b52e9-114">-AsJob</span></span>
<span data-ttu-id="b52e9-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="b52e9-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b52e9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b52e9-116">-DefaultProfile</span></span>
<span data-ttu-id="b52e9-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b52e9-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b52e9-118">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="b52e9-118">-Force</span></span>
<span data-ttu-id="b52e9-119">Wymuszanie usuwania opcji</span><span class="sxs-lookup"><span data-stu-id="b52e9-119">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="b52e9-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b52e9-120">-Name</span></span>
<span data-ttu-id="b52e9-121">Nazwa aplikacji WebApp</span><span class="sxs-lookup"><span data-stu-id="b52e9-121">WebApp Name</span></span>

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

### <span data-ttu-id="b52e9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b52e9-122">-ResourceGroupName</span></span>
<span data-ttu-id="b52e9-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="b52e9-123">Resource Group Name</span></span>

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

### <span data-ttu-id="b52e9-124">- WebApp</span><span class="sxs-lookup"><span data-stu-id="b52e9-124">-WebApp</span></span>
<span data-ttu-id="b52e9-125">Obiekt WebApp</span><span class="sxs-lookup"><span data-stu-id="b52e9-125">WebApp Object</span></span>

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

### <span data-ttu-id="b52e9-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b52e9-126">-Confirm</span></span>
<span data-ttu-id="b52e9-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie. Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b52e9-127">Prompts you for confirmation before running the cmdlet.Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b52e9-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b52e9-128">-WhatIf</span></span>
<span data-ttu-id="b52e9-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b52e9-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b52e9-130">Polecenie cmdlet nie zostanie uruchomione. Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b52e9-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b52e9-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b52e9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b52e9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b52e9-132">CommonParameters</span></span>
<span data-ttu-id="b52e9-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b52e9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b52e9-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b52e9-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b52e9-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b52e9-135">INPUTS</span></span>

### <span data-ttu-id="b52e9-136">System.String</span><span class="sxs-lookup"><span data-stu-id="b52e9-136">System.String</span></span>

### <span data-ttu-id="b52e9-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="b52e9-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="b52e9-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b52e9-138">OUTPUTS</span></span>

### <span data-ttu-id="b52e9-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="b52e9-139">System.Void</span></span>

## <span data-ttu-id="b52e9-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b52e9-140">NOTES</span></span>

## <span data-ttu-id="b52e9-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b52e9-141">RELATED LINKS</span></span>

[<span data-ttu-id="b52e9-142">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b52e9-142">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="b52e9-143">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b52e9-143">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="b52e9-144">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b52e9-144">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="b52e9-145">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b52e9-145">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="b52e9-146">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b52e9-146">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


