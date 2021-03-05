---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/enter-azwebappcontainerpssession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Enter-AzWebAppContainerPSSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Enter-AzWebAppContainerPSSession.md
ms.openlocfilehash: e889e3f8d3d94993494c10141629eee6dceed01c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972385"
---
# <span data-ttu-id="7e4dc-101">Enter-AzWebAppContainerPSSession</span><span class="sxs-lookup"><span data-stu-id="7e4dc-101">Enter-AzWebAppContainerPSSession</span></span>

## <span data-ttu-id="7e4dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e4dc-102">SYNOPSIS</span></span>
<span data-ttu-id="7e4dc-103">Otwiera zdalną sesję programu PowerShell w kontenerze systemu Windows określonym w określonej witrynie lub przedziale i w danej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-103">Opens a remote PowerShell session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="7e4dc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7e4dc-104">SYNTAX</span></span>

### <span data-ttu-id="7e4dc-105">S1 (domyślne)</span><span class="sxs-lookup"><span data-stu-id="7e4dc-105">S1 (Default)</span></span>
```
Enter-AzWebAppContainerPSSession [-PassThru] [-Force] [[-SlotName] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e4dc-106">S2</span><span class="sxs-lookup"><span data-stu-id="7e4dc-106">S2</span></span>
```
Enter-AzWebAppContainerPSSession [-PassThru] [-Force] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e4dc-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="7e4dc-107">DESCRIPTION</span></span>
<span data-ttu-id="7e4dc-108">Otwiera zdalną sesję programu PowerShell w kontenerze systemu Windows określonym w określonej witrynie lub przedziale i danej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-108">opens a remote PowerShell session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="7e4dc-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7e4dc-109">EXAMPLES</span></span>

### <span data-ttu-id="7e4dc-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7e4dc-110">Example 1</span></span>
```
PS C:\> Enter-AzWebAppContainerPSSession -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="7e4dc-111">To polecenie powoduje otwarcie zdalnej sesji programu PowerShell w aplikacji kontenera systemu Windows ContosoASP</span><span class="sxs-lookup"><span data-stu-id="7e4dc-111">This command opens a remote PowerShell session into the windows container app ContosoASP</span></span>

## <span data-ttu-id="7e4dc-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7e4dc-112">PARAMETERS</span></span>

### <span data-ttu-id="7e4dc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e4dc-113">-DefaultProfile</span></span>
<span data-ttu-id="7e4dc-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e4dc-115">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="7e4dc-115">-Force</span></span>
<span data-ttu-id="7e4dc-116">Utwórz sesję programu PowerShell bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-116">Create the PowerShell session without prompting for confirmation.</span></span>

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

### <span data-ttu-id="7e4dc-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="7e4dc-117">-Name</span></span>
<span data-ttu-id="7e4dc-118">Nazwa aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-118">The name of the web app.</span></span>

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

### <span data-ttu-id="7e4dc-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7e4dc-119">-PassThru</span></span>
<span data-ttu-id="7e4dc-120">Zwraca wartość wskazującą sukces lub porażkę.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-120">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="7e4dc-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e4dc-121">-ResourceGroupName</span></span>
<span data-ttu-id="7e4dc-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="7e4dc-123">-SlotName</span><span class="sxs-lookup"><span data-stu-id="7e4dc-123">-SlotName</span></span>
<span data-ttu-id="7e4dc-124">Nazwa miejsca aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-124">The name of the web app slot.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e4dc-125">- WebApp</span><span class="sxs-lookup"><span data-stu-id="7e4dc-125">-WebApp</span></span>
<span data-ttu-id="7e4dc-126">Obiekt aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="7e4dc-126">The web app object</span></span>

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

### <span data-ttu-id="7e4dc-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7e4dc-127">-Confirm</span></span>
<span data-ttu-id="7e4dc-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e4dc-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e4dc-129">-WhatIf</span></span>
<span data-ttu-id="7e4dc-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7e4dc-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e4dc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e4dc-132">CommonParameters</span></span>
<span data-ttu-id="7e4dc-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e4dc-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e4dc-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e4dc-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7e4dc-135">INPUTS</span></span>

### <span data-ttu-id="7e4dc-136">System.String</span><span class="sxs-lookup"><span data-stu-id="7e4dc-136">System.String</span></span>

### <span data-ttu-id="7e4dc-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="7e4dc-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="7e4dc-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7e4dc-138">OUTPUTS</span></span>

### <span data-ttu-id="7e4dc-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="7e4dc-139">System.Void</span></span>

## <span data-ttu-id="7e4dc-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7e4dc-140">NOTES</span></span>

## <span data-ttu-id="7e4dc-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7e4dc-141">RELATED LINKS</span></span>
