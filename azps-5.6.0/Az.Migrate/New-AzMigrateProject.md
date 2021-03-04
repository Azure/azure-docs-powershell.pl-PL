---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/new-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateProject.md
ms.openlocfilehash: 8b3a14c9e8416c1ffc9809d09d664b7809f53a1d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982689"
---
# <span data-ttu-id="c9406-101">New-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="c9406-101">New-AzMigrateProject</span></span>

## <span data-ttu-id="c9406-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9406-102">SYNOPSIS</span></span>
<span data-ttu-id="c9406-103">Tworzy nowy projekt migracji.</span><span class="sxs-lookup"><span data-stu-id="c9406-103">Creates a new Migrate project.</span></span>

## <span data-ttu-id="c9406-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c9406-104">SYNTAX</span></span>

```
New-AzMigrateProject -Location <String> -Name <String> -ResourceGroupName <String> [-ETag <String>]
 [-Property <IMigrateProjectProperties>] [-SubscriptionId <String>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c9406-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="c9406-105">DESCRIPTION</span></span>
<span data-ttu-id="c9406-106">Tworzy nowy projekt migracji.</span><span class="sxs-lookup"><span data-stu-id="c9406-106">Creates a new Migrate project.</span></span>

## <span data-ttu-id="c9406-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c9406-107">EXAMPLES</span></span>

### <span data-ttu-id="c9406-108">Przykład 1. Tworzenie (domyślne)</span><span class="sxs-lookup"><span data-stu-id="c9406-108">Example 1: Create (Default)</span></span>
```powershell
PS C:\> New-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName kuchaturimpkocrg1 -Name kuchaturimpkocrg1pwshp14 -Location "centralus"

ETag Location  Name                     Type
---- --------  ----                     ----
     centralus kuchaturimpkocrg1pwshp14 Microsoft.Migrate/MigrateProjects

```

<span data-ttu-id="c9406-109">Metoda tworzenia nowego projektu migracji.</span><span class="sxs-lookup"><span data-stu-id="c9406-109">Method to create a new migrate project.</span></span>

## <span data-ttu-id="c9406-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c9406-110">PARAMETERS</span></span>

### <span data-ttu-id="c9406-111">— ETag</span><span class="sxs-lookup"><span data-stu-id="c9406-111">-ETag</span></span>
<span data-ttu-id="c9406-112">Określa nazwę komputera V Machine.</span><span class="sxs-lookup"><span data-stu-id="c9406-112">Specifies the VMware machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9406-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="c9406-113">-Location</span></span>
<span data-ttu-id="c9406-114">Określa nazwę komputera V Machine.</span><span class="sxs-lookup"><span data-stu-id="c9406-114">Specifies the VMware machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9406-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c9406-115">-Name</span></span>
<span data-ttu-id="c9406-116">Określa nazwę migrowania projektu.</span><span class="sxs-lookup"><span data-stu-id="c9406-116">Specifies the migrate project name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9406-117">- Właściwość</span><span class="sxs-lookup"><span data-stu-id="c9406-117">-Property</span></span>
<span data-ttu-id="c9406-118">Określa właściwości projektu.</span><span class="sxs-lookup"><span data-stu-id="c9406-118">Specifies the project properties.</span></span>
<span data-ttu-id="c9406-119">Aby utworzyć tabelę, zobacz sekcję NOTATKI, aby uzyskać informacje o właściwościach WŁAŚCIWOŚCI i utworzyć tabelę skrótu.</span><span class="sxs-lookup"><span data-stu-id="c9406-119">To construct, see NOTES section for PROPERTY properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.IMigrateProjectProperties
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9406-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9406-120">-ResourceGroupName</span></span>
<span data-ttu-id="c9406-121">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c9406-121">Specifies the resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9406-122">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c9406-122">-SubscriptionId</span></span>
<span data-ttu-id="c9406-123">Określa identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="c9406-123">Specifies the subscription id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9406-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c9406-124">-Confirm</span></span>
<span data-ttu-id="c9406-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c9406-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9406-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9406-126">-WhatIf</span></span>
<span data-ttu-id="c9406-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9406-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9406-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c9406-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9406-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9406-129">CommonParameters</span></span>
<span data-ttu-id="c9406-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9406-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9406-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c9406-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9406-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c9406-132">INPUTS</span></span>

## <span data-ttu-id="c9406-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c9406-133">OUTPUTS</span></span>

## <span data-ttu-id="c9406-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c9406-134">NOTES</span></span>

<span data-ttu-id="c9406-135">ALIASY</span><span class="sxs-lookup"><span data-stu-id="c9406-135">ALIASES</span></span>

<span data-ttu-id="c9406-136">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c9406-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c9406-137">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="c9406-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c9406-138">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c9406-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c9406-139">WŁAŚCIWOŚĆ: <IMigrateProjectProperties> określa właściwości projektu.</span><span class="sxs-lookup"><span data-stu-id="c9406-139">PROPERTY <IMigrateProjectProperties>: Specifies the project properties.</span></span>
  - <span data-ttu-id="c9406-140">`[ProvisioningState <ProvisioningState?>]`: stan inicjowania obsługi administracyjnej projektu migracji.</span><span class="sxs-lookup"><span data-stu-id="c9406-140">`[ProvisioningState <ProvisioningState?>]`: Provisioning state of the migrate project.</span></span>
  - <span data-ttu-id="c9406-141">`[RegisteredTool <String[]>]`: pobiera lub ustawia listę narzędzi zarejestrowanych w projekcie migracji.</span><span class="sxs-lookup"><span data-stu-id="c9406-141">`[RegisteredTool <String[]>]`: Gets or sets the list of tools registered with the migrate project.</span></span>

## <span data-ttu-id="c9406-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c9406-142">RELATED LINKS</span></span>

