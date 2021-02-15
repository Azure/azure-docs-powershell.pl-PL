---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateProject.md
ms.openlocfilehash: 32c4799f574e94eecee1f7ebf810c2f27bc5eccf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203582"
---
# <span data-ttu-id="1c92d-101">New-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="1c92d-101">New-AzMigrateProject</span></span>

## <span data-ttu-id="1c92d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c92d-102">SYNOPSIS</span></span>
<span data-ttu-id="1c92d-103">Tworzy nowy projekt migracji.</span><span class="sxs-lookup"><span data-stu-id="1c92d-103">Creates a new Migrate project.</span></span>

## <span data-ttu-id="1c92d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1c92d-104">SYNTAX</span></span>

```
New-AzMigrateProject -Location <String> -Name <String> -ResourceGroupName <String> [-ETag <String>]
 [-Property <IMigrateProjectProperties>] [-SubscriptionId <String>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1c92d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="1c92d-105">DESCRIPTION</span></span>
<span data-ttu-id="1c92d-106">Tworzy nowy projekt migracji.</span><span class="sxs-lookup"><span data-stu-id="1c92d-106">Creates a new Migrate project.</span></span>

## <span data-ttu-id="1c92d-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1c92d-107">EXAMPLES</span></span>

### <span data-ttu-id="1c92d-108">Przykład 1. Tworzenie (domyślne)</span><span class="sxs-lookup"><span data-stu-id="1c92d-108">Example 1: Create (Default)</span></span>
```powershell
PS C:\> New-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName kuchaturimpkocrg1 -Name kuchaturimpkocrg1pwshp14 -Location "centralus"

ETag Location  Name                     Type
---- --------  ----                     ----
     centralus kuchaturimpkocrg1pwshp14 Microsoft.Migrate/MigrateProjects

```

<span data-ttu-id="1c92d-109">Metoda tworzenia nowego projektu migracji.</span><span class="sxs-lookup"><span data-stu-id="1c92d-109">Method to create a new migrate project.</span></span>

## <span data-ttu-id="1c92d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1c92d-110">PARAMETERS</span></span>

### <span data-ttu-id="1c92d-111">— ETag</span><span class="sxs-lookup"><span data-stu-id="1c92d-111">-ETag</span></span>
<span data-ttu-id="1c92d-112">Określa nazwę komputera V Machine.</span><span class="sxs-lookup"><span data-stu-id="1c92d-112">Specifies the VMware machine name.</span></span>

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

### <span data-ttu-id="1c92d-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="1c92d-113">-Location</span></span>
<span data-ttu-id="1c92d-114">Określa nazwę komputera V Machine.</span><span class="sxs-lookup"><span data-stu-id="1c92d-114">Specifies the VMware machine name.</span></span>

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

### <span data-ttu-id="1c92d-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="1c92d-115">-Name</span></span>
<span data-ttu-id="1c92d-116">Określa nazwę migrowania projektu.</span><span class="sxs-lookup"><span data-stu-id="1c92d-116">Specifies the migrate project name.</span></span>

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

### <span data-ttu-id="1c92d-117">- Właściwość</span><span class="sxs-lookup"><span data-stu-id="1c92d-117">-Property</span></span>
<span data-ttu-id="1c92d-118">Określa właściwości projektu.</span><span class="sxs-lookup"><span data-stu-id="1c92d-118">Specifies the project properties.</span></span>
<span data-ttu-id="1c92d-119">Aby skonstruować, zobacz sekcję NOTATKI, aby uzyskać informacje o właściwościach WŁAŚCIWOŚCI i utworzyć tabelę skrótu.</span><span class="sxs-lookup"><span data-stu-id="1c92d-119">To construct, see NOTES section for PROPERTY properties and create a hash table.</span></span>

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

### <span data-ttu-id="1c92d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c92d-120">-ResourceGroupName</span></span>
<span data-ttu-id="1c92d-121">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1c92d-121">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="1c92d-122">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1c92d-122">-SubscriptionId</span></span>
<span data-ttu-id="1c92d-123">Określa identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="1c92d-123">Specifies the subscription id.</span></span>

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

### <span data-ttu-id="1c92d-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1c92d-124">-Confirm</span></span>
<span data-ttu-id="1c92d-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1c92d-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c92d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c92d-126">-WhatIf</span></span>
<span data-ttu-id="1c92d-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c92d-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c92d-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1c92d-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c92d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c92d-129">CommonParameters</span></span>
<span data-ttu-id="1c92d-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c92d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c92d-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1c92d-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c92d-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1c92d-132">INPUTS</span></span>

## <span data-ttu-id="1c92d-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1c92d-133">OUTPUTS</span></span>

## <span data-ttu-id="1c92d-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1c92d-134">NOTES</span></span>

<span data-ttu-id="1c92d-135">ALIASY</span><span class="sxs-lookup"><span data-stu-id="1c92d-135">ALIASES</span></span>

<span data-ttu-id="1c92d-136">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="1c92d-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1c92d-137">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="1c92d-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1c92d-138">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1c92d-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1c92d-139">WŁAŚCIWOŚĆ: <IMigrateProjectProperties> Określa właściwości projektu.</span><span class="sxs-lookup"><span data-stu-id="1c92d-139">PROPERTY <IMigrateProjectProperties>: Specifies the project properties.</span></span>
  - <span data-ttu-id="1c92d-140">`[ProvisioningState <ProvisioningState?>]`: stan inicjowania obsługi administracyjnej projektu migracji.</span><span class="sxs-lookup"><span data-stu-id="1c92d-140">`[ProvisioningState <ProvisioningState?>]`: Provisioning state of the migrate project.</span></span>
  - <span data-ttu-id="1c92d-141">`[RegisteredTool <String[]>]`: pobiera lub ustawia listę narzędzi zarejestrowanych w projekcie migracji.</span><span class="sxs-lookup"><span data-stu-id="1c92d-141">`[RegisteredTool <String[]>]`: Gets or sets the list of tools registered with the migrate project.</span></span>

## <span data-ttu-id="1c92d-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1c92d-142">RELATED LINKS</span></span>

