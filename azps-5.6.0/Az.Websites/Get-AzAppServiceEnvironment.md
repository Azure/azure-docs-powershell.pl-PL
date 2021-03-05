---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azappserviceenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServiceEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServiceEnvironment.md
ms.openlocfilehash: 9641c55dd25d8f09d1898bdda37fafa840db0a19
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983898"
---
# <span data-ttu-id="6893b-101">Get-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="6893b-101">Get-AzAppServiceEnvironment</span></span>

## <span data-ttu-id="6893b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6893b-102">SYNOPSIS</span></span>
<span data-ttu-id="6893b-103">Pobiera środowisko usługi aplikacji.</span><span class="sxs-lookup"><span data-stu-id="6893b-103">Gets App Service Environment.</span></span> <span data-ttu-id="6893b-104">Jeśli zostanie określona tylko grupa zasobów, zwróci ona listę ase w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="6893b-104">If only Resource Group is specified, it will return a list of ASE in the Resource Group.</span></span>

## <span data-ttu-id="6893b-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6893b-105">SYNTAX</span></span>

```
Get-AzAppServiceEnvironment [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6893b-106">OPIS</span><span class="sxs-lookup"><span data-stu-id="6893b-106">DESCRIPTION</span></span>
<span data-ttu-id="6893b-107">Polecenie **cmdlet Get-AzAppServiceEnvironment** zwraca ase pasujące do zapytania.</span><span class="sxs-lookup"><span data-stu-id="6893b-107">The **Get-AzAppServiceEnvironment** cmdlet return ASE(s) matching the query.</span></span>

## <span data-ttu-id="6893b-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6893b-108">EXAMPLES</span></span>

### <span data-ttu-id="6893b-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6893b-109">Example 1</span></span>
```powershell
PS C:\> Get-AzAppServiceEnvironment -ResourceGroupName MyResourceGroup -Name MyAseName
```

<span data-ttu-id="6893b-110">Zwraca określone środowisko usługi aplikacji <MyAseName> o nazwie <MyResourceGroup></span><span class="sxs-lookup"><span data-stu-id="6893b-110">Returns a specific App Service Environment named <MyAseName> in <MyResourceGroup></span></span>

## <span data-ttu-id="6893b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6893b-111">PARAMETERS</span></span>

### <span data-ttu-id="6893b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6893b-112">-DefaultProfile</span></span>
<span data-ttu-id="6893b-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6893b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6893b-114">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="6893b-114">-Name</span></span>
<span data-ttu-id="6893b-115">Nazwa środowiska usługi aplikacji.</span><span class="sxs-lookup"><span data-stu-id="6893b-115">The name of the app service environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6893b-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6893b-116">-ResourceGroupName</span></span>
<span data-ttu-id="6893b-117">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6893b-117">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6893b-118">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6893b-118">-Confirm</span></span>
<span data-ttu-id="6893b-119">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6893b-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6893b-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6893b-120">-WhatIf</span></span>
<span data-ttu-id="6893b-121">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6893b-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6893b-122">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="6893b-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6893b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6893b-123">CommonParameters</span></span>
<span data-ttu-id="6893b-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6893b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6893b-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6893b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6893b-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6893b-126">INPUTS</span></span>

### <span data-ttu-id="6893b-127">Brak</span><span class="sxs-lookup"><span data-stu-id="6893b-127">None</span></span>

## <span data-ttu-id="6893b-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6893b-128">OUTPUTS</span></span>

### <span data-ttu-id="6893b-129">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="6893b-129">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServiceEnvironment</span></span>

## <span data-ttu-id="6893b-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6893b-130">NOTES</span></span>

## <span data-ttu-id="6893b-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6893b-131">RELATED LINKS</span></span>

[<span data-ttu-id="6893b-132">New-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="6893b-132">New-AzAppServiceEnvironment</span></span>](./New-AzAppServiceEnvironment.md)

[<span data-ttu-id="6893b-133">New-AzAppServiceEnvironmentInboundServices</span><span class="sxs-lookup"><span data-stu-id="6893b-133">New-AzAppServiceEnvironmentInboundServices</span></span>](./New-AzAppServiceEnvironmentInboundServices.md)

[<span data-ttu-id="6893b-134">Remove-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="6893b-134">Remove-AzAppServiceEnvironment</span></span>](./Remove-AzAppServiceEnvironment.md)