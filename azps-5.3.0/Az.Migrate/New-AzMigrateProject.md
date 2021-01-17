---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateProject.md
ms.openlocfilehash: 32c4799f574e94eecee1f7ebf810c2f27bc5eccf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385749"
---
# <span data-ttu-id="306ab-101">New-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="306ab-101">New-AzMigrateProject</span></span>

## <span data-ttu-id="306ab-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="306ab-102">SYNOPSIS</span></span>
<span data-ttu-id="306ab-103">Tworzy nowy projekt migracji.</span><span class="sxs-lookup"><span data-stu-id="306ab-103">Creates a new Migrate project.</span></span>

## <span data-ttu-id="306ab-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="306ab-104">SYNTAX</span></span>

```
New-AzMigrateProject -Location <String> -Name <String> -ResourceGroupName <String> [-ETag <String>]
 [-Property <IMigrateProjectProperties>] [-SubscriptionId <String>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="306ab-105">Opis</span><span class="sxs-lookup"><span data-stu-id="306ab-105">DESCRIPTION</span></span>
<span data-ttu-id="306ab-106">Tworzy nowy projekt migracji.</span><span class="sxs-lookup"><span data-stu-id="306ab-106">Creates a new Migrate project.</span></span>

## <span data-ttu-id="306ab-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="306ab-107">EXAMPLES</span></span>

### <span data-ttu-id="306ab-108">Przykład 1. Tworzenie (domyślne)</span><span class="sxs-lookup"><span data-stu-id="306ab-108">Example 1: Create (Default)</span></span>
```powershell
PS C:\> New-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName kuchaturimpkocrg1 -Name kuchaturimpkocrg1pwshp14 -Location "centralus"

ETag Location  Name                     Type
---- --------  ----                     ----
     centralus kuchaturimpkocrg1pwshp14 Microsoft.Migrate/MigrateProjects

```

<span data-ttu-id="306ab-109">Metoda tworzenia nowego projektu migracji.</span><span class="sxs-lookup"><span data-stu-id="306ab-109">Method to create a new migrate project.</span></span>

## <span data-ttu-id="306ab-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="306ab-110">PARAMETERS</span></span>

### <span data-ttu-id="306ab-111">-ETag</span><span class="sxs-lookup"><span data-stu-id="306ab-111">-ETag</span></span>
<span data-ttu-id="306ab-112">Określa nazwę komputera VMware.</span><span class="sxs-lookup"><span data-stu-id="306ab-112">Specifies the VMware machine name.</span></span>

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

### <span data-ttu-id="306ab-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="306ab-113">-Location</span></span>
<span data-ttu-id="306ab-114">Określa nazwę komputera VMware.</span><span class="sxs-lookup"><span data-stu-id="306ab-114">Specifies the VMware machine name.</span></span>

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

### <span data-ttu-id="306ab-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="306ab-115">-Name</span></span>
<span data-ttu-id="306ab-116">Określa nazwę projektu migracji.</span><span class="sxs-lookup"><span data-stu-id="306ab-116">Specifies the migrate project name.</span></span>

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

### <span data-ttu-id="306ab-117">-Property</span><span class="sxs-lookup"><span data-stu-id="306ab-117">-Property</span></span>
<span data-ttu-id="306ab-118">Określa właściwości projektu.</span><span class="sxs-lookup"><span data-stu-id="306ab-118">Specifies the project properties.</span></span>
<span data-ttu-id="306ab-119">Aby skonstruować, zobacz sekcję notatki dla właściwości właściwości i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="306ab-119">To construct, see NOTES section for PROPERTY properties and create a hash table.</span></span>

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

### <span data-ttu-id="306ab-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="306ab-120">-ResourceGroupName</span></span>
<span data-ttu-id="306ab-121">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="306ab-121">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="306ab-122">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="306ab-122">-SubscriptionId</span></span>
<span data-ttu-id="306ab-123">Określa identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="306ab-123">Specifies the subscription id.</span></span>

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

### <span data-ttu-id="306ab-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="306ab-124">-Confirm</span></span>
<span data-ttu-id="306ab-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="306ab-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="306ab-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="306ab-126">-WhatIf</span></span>
<span data-ttu-id="306ab-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="306ab-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="306ab-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="306ab-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="306ab-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="306ab-129">CommonParameters</span></span>
<span data-ttu-id="306ab-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="306ab-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="306ab-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="306ab-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="306ab-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="306ab-132">INPUTS</span></span>

## <span data-ttu-id="306ab-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="306ab-133">OUTPUTS</span></span>

## <span data-ttu-id="306ab-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="306ab-134">NOTES</span></span>

<span data-ttu-id="306ab-135">PISUJE</span><span class="sxs-lookup"><span data-stu-id="306ab-135">ALIASES</span></span>

<span data-ttu-id="306ab-136">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="306ab-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="306ab-137">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="306ab-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="306ab-138">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="306ab-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="306ab-139">Właściwość <IMigrateProjectProperties> : określa właściwości projektu.</span><span class="sxs-lookup"><span data-stu-id="306ab-139">PROPERTY <IMigrateProjectProperties>: Specifies the project properties.</span></span>
  - <span data-ttu-id="306ab-140">`[ProvisioningState <ProvisioningState?>]`: Stan inicjowania obsługi projektu migracji.</span><span class="sxs-lookup"><span data-stu-id="306ab-140">`[ProvisioningState <ProvisioningState?>]`: Provisioning state of the migrate project.</span></span>
  - <span data-ttu-id="306ab-141">`[RegisteredTool <String[]>]`: Pobiera lub ustawia listę narzędzi zarejestrowanych w projekcie migracji.</span><span class="sxs-lookup"><span data-stu-id="306ab-141">`[RegisteredTool <String[]>]`: Gets or sets the list of tools registered with the migrate project.</span></span>

## <span data-ttu-id="306ab-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="306ab-142">RELATED LINKS</span></span>

