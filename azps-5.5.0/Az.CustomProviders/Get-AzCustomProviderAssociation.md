---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/get-azcustomproviderassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProviderAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProviderAssociation.md
ms.openlocfilehash: 08d760c73256b71842fac36a7d095db2aab21128
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196667"
---
# <span data-ttu-id="2691c-101">Get-AzCustomProviderAssociation</span><span class="sxs-lookup"><span data-stu-id="2691c-101">Get-AzCustomProviderAssociation</span></span>

## <span data-ttu-id="2691c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2691c-102">SYNOPSIS</span></span>
<span data-ttu-id="2691c-103">Pobierz skojarzenie.</span><span class="sxs-lookup"><span data-stu-id="2691c-103">Get an association.</span></span>

## <span data-ttu-id="2691c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2691c-104">SYNTAX</span></span>

### <span data-ttu-id="2691c-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="2691c-105">List (Default)</span></span>
```
Get-AzCustomProviderAssociation -Scope <String> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2691c-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="2691c-106">Get</span></span>
```
Get-AzCustomProviderAssociation -Name <String> -Scope <String> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="2691c-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2691c-107">GetViaIdentity</span></span>
```
Get-AzCustomProviderAssociation -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="2691c-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="2691c-108">DESCRIPTION</span></span>
<span data-ttu-id="2691c-109">Pobierz skojarzenie.</span><span class="sxs-lookup"><span data-stu-id="2691c-109">Get an association.</span></span>

## <span data-ttu-id="2691c-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2691c-110">EXAMPLES</span></span>

### <span data-ttu-id="2691c-111">Przykład 1. Lista niestandardowych skojarzeń dostawców</span><span class="sxs-lookup"><span data-stu-id="2691c-111">Example 1: List custom provider associations</span></span>
```powershell
PS C:\> Get-AzCustomProviderAssociation

Location  Name             Type
--------  ----             ----
East US 2 MyAssoc   Microsoft.CustomProviders/associations
```

<span data-ttu-id="2691c-112">Lista wszystkich niestandardowych skojarzeń dostawców dla danego zakresu.</span><span class="sxs-lookup"><span data-stu-id="2691c-112">List all custom provider associations for a given scope.</span></span>

### <span data-ttu-id="2691c-113">Przykład 2. Uzyskiwanie skojarzenia</span><span class="sxs-lookup"><span data-stu-id="2691c-113">Example 2: Get an association</span></span>
```powershell
PS C:\> Get-AzCustomProviderAssociation -Scope $resourceId -Name MyAssoc

Location  Name             Type
--------  ----             ----
East US 2 MyAssoc   Microsoft.CustomProviders/associations
```

<span data-ttu-id="2691c-114">Uzyskiwanie szczegółów dotyczących pojedynczego skojarzenia customProvider</span><span class="sxs-lookup"><span data-stu-id="2691c-114">Get details for a single CustomProvider association</span></span>

## <span data-ttu-id="2691c-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2691c-115">PARAMETERS</span></span>

### <span data-ttu-id="2691c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2691c-116">-DefaultProfile</span></span>
<span data-ttu-id="2691c-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2691c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2691c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2691c-118">-InputObject</span></span>
<span data-ttu-id="2691c-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="2691c-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2691c-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="2691c-120">-Name</span></span>
<span data-ttu-id="2691c-121">Nazwa skojarzenia.</span><span class="sxs-lookup"><span data-stu-id="2691c-121">The name of the association.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AssociationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2691c-122">— Zakres</span><span class="sxs-lookup"><span data-stu-id="2691c-122">-Scope</span></span>
<span data-ttu-id="2691c-123">Zakres skojarzenia.</span><span class="sxs-lookup"><span data-stu-id="2691c-123">The scope of the association.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2691c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2691c-124">CommonParameters</span></span>
<span data-ttu-id="2691c-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2691c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2691c-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2691c-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2691c-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2691c-127">INPUTS</span></span>

### <span data-ttu-id="2691c-128">Microsoft.Azure.PowerShell.Cmdlet.CustomProviders.Models.ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="2691c-128">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="2691c-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2691c-129">OUTPUTS</span></span>

### <span data-ttu-id="2691c-130">Microsoft.Azure.PowerShell.Cmdlet.CustomProviders.Models.Api20180901Preview.IAssociation</span><span class="sxs-lookup"><span data-stu-id="2691c-130">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.IAssociation</span></span>

## <span data-ttu-id="2691c-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2691c-131">NOTES</span></span>

<span data-ttu-id="2691c-132">ALIASY</span><span class="sxs-lookup"><span data-stu-id="2691c-132">ALIASES</span></span>

<span data-ttu-id="2691c-133">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="2691c-133">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2691c-134">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="2691c-134">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2691c-135">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2691c-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2691c-136">INPUTOBJECT: <ICustomProvidersIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="2691c-136">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2691c-137">`[AssociationName <String>]`: nazwa skojarzenia.</span><span class="sxs-lookup"><span data-stu-id="2691c-137">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="2691c-138">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="2691c-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2691c-139">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2691c-139">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="2691c-140">`[ResourceProviderName <String>]`: nazwa dostawcy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2691c-140">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="2691c-141">`[Scope <String>]`: zakres skojarzenia.</span><span class="sxs-lookup"><span data-stu-id="2691c-141">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="2691c-142">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2691c-142">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="2691c-143">Jest to ciąg w formacie GUID (np. 000000000-0000-0000-0000-0000000000000)</span><span class="sxs-lookup"><span data-stu-id="2691c-143">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="2691c-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2691c-144">RELATED LINKS</span></span>

