---
external help file: ''
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcegraph/remove-azresourcegraphquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Remove-AzResourceGraphQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Remove-AzResourceGraphQuery.md
ms.openlocfilehash: 3fc5c493f94b6da371a4249479e397ea6e2362f0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377918"
---
# <span data-ttu-id="51a07-101">Remove-AzResourceGraphQuery</span><span class="sxs-lookup"><span data-stu-id="51a07-101">Remove-AzResourceGraphQuery</span></span>

## <span data-ttu-id="51a07-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="51a07-102">SYNOPSIS</span></span>
<span data-ttu-id="51a07-103">Usuwanie zapytania dotyczącego wykresu.</span><span class="sxs-lookup"><span data-stu-id="51a07-103">Delete a graph query.</span></span>

## <span data-ttu-id="51a07-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="51a07-104">SYNTAX</span></span>

### <span data-ttu-id="51a07-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="51a07-105">Delete (Default)</span></span>
```
Remove-AzResourceGraphQuery -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="51a07-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="51a07-106">DeleteViaIdentity</span></span>
```
Remove-AzResourceGraphQuery -InputObject <IResourceGraphIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="51a07-107">Opis</span><span class="sxs-lookup"><span data-stu-id="51a07-107">DESCRIPTION</span></span>
<span data-ttu-id="51a07-108">Usuwanie zapytania dotyczącego wykresu.</span><span class="sxs-lookup"><span data-stu-id="51a07-108">Delete a graph query.</span></span>

## <span data-ttu-id="51a07-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="51a07-109">EXAMPLES</span></span>

### <span data-ttu-id="51a07-110">Przykład 1: usuwanie zapytania dotyczącego wykresu zasobów według nazwy</span><span class="sxs-lookup"><span data-stu-id="51a07-110">Example 1: Remove a resource graph query by name</span></span>
```powershell
PS C:\> Remove-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t03

```

<span data-ttu-id="51a07-111">To polecenie usuwa zapytanie wykresu zasobu według nazwy.</span><span class="sxs-lookup"><span data-stu-id="51a07-111">This command removes a resource graph query by name.</span></span>

### <span data-ttu-id="51a07-112">Przykład 2: usuwanie zapytania dotyczącego wykresu zasobów według obiektów</span><span class="sxs-lookup"><span data-stu-id="51a07-112">Example 2: Remove a resource graph query by object</span></span>
```powershell
PS C:\> $query = Get-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t02
PS C:\> Remove-AzResourceGraphQuery -InputObject $query 

```

<span data-ttu-id="51a07-113">To polecenie usuwa zapytanie wykresu zasobu według obiektu.</span><span class="sxs-lookup"><span data-stu-id="51a07-113">This command removes a resource graph query by object.</span></span>

## <span data-ttu-id="51a07-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="51a07-114">PARAMETERS</span></span>

### <span data-ttu-id="51a07-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51a07-115">-DefaultProfile</span></span>
<span data-ttu-id="51a07-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="51a07-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51a07-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="51a07-117">-InputObject</span></span>
<span data-ttu-id="51a07-118">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="51a07-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51a07-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="51a07-119">-Name</span></span>
<span data-ttu-id="51a07-120">Nazwa zasobu kwerendy wykresu.</span><span class="sxs-lookup"><span data-stu-id="51a07-120">The name of the Graph Query resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51a07-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="51a07-121">-PassThru</span></span>
<span data-ttu-id="51a07-122">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="51a07-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="51a07-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51a07-123">-ResourceGroupName</span></span>
<span data-ttu-id="51a07-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="51a07-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51a07-125">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="51a07-125">-SubscriptionId</span></span>
<span data-ttu-id="51a07-126">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="51a07-126">The Azure subscription Id.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51a07-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="51a07-127">-Confirm</span></span>
<span data-ttu-id="51a07-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51a07-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51a07-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51a07-129">-WhatIf</span></span>
<span data-ttu-id="51a07-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51a07-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51a07-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="51a07-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51a07-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51a07-132">CommonParameters</span></span>
<span data-ttu-id="51a07-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51a07-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51a07-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="51a07-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51a07-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="51a07-135">INPUTS</span></span>

### <span data-ttu-id="51a07-136">Microsoft. Azure. PowerShell. polecenia. ResourceGraph. models. IResourceGraphIdentity</span><span class="sxs-lookup"><span data-stu-id="51a07-136">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span></span>

## <span data-ttu-id="51a07-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="51a07-137">OUTPUTS</span></span>

### <span data-ttu-id="51a07-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="51a07-138">System.Boolean</span></span>

## <span data-ttu-id="51a07-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="51a07-139">NOTES</span></span>

<span data-ttu-id="51a07-140">PISUJE</span><span class="sxs-lookup"><span data-stu-id="51a07-140">ALIASES</span></span>

<span data-ttu-id="51a07-141">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="51a07-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="51a07-142">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="51a07-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="51a07-143">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="51a07-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="51a07-144">INPUTobject <IResourceGraphIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="51a07-144">INPUTOBJECT <IResourceGraphIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="51a07-145">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="51a07-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="51a07-146">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="51a07-146">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="51a07-147">`[ResourceName <String>]`: Nazwa zasobu kwerendy wykresu.</span><span class="sxs-lookup"><span data-stu-id="51a07-147">`[ResourceName <String>]`: The name of the Graph Query resource.</span></span>
  - <span data-ttu-id="51a07-148">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="51a07-148">`[SubscriptionId <String>]`: The Azure subscription Id.</span></span>

## <span data-ttu-id="51a07-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="51a07-149">RELATED LINKS</span></span>

