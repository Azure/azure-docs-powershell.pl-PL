---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/get-azcustomproviderassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProviderAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProviderAssociation.md
ms.openlocfilehash: 08d760c73256b71842fac36a7d095db2aab21128
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369173"
---
# <span data-ttu-id="cc3ec-101">Get-AzCustomProviderAssociation</span><span class="sxs-lookup"><span data-stu-id="cc3ec-101">Get-AzCustomProviderAssociation</span></span>

## <span data-ttu-id="cc3ec-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cc3ec-102">SYNOPSIS</span></span>
<span data-ttu-id="cc3ec-103">Uzyskaj powiązanie.</span><span class="sxs-lookup"><span data-stu-id="cc3ec-103">Get an association.</span></span>

## <span data-ttu-id="cc3ec-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cc3ec-104">SYNTAX</span></span>

### <span data-ttu-id="cc3ec-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="cc3ec-105">List (Default)</span></span>
```
Get-AzCustomProviderAssociation -Scope <String> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="cc3ec-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="cc3ec-106">Get</span></span>
```
Get-AzCustomProviderAssociation -Name <String> -Scope <String> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="cc3ec-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cc3ec-107">GetViaIdentity</span></span>
```
Get-AzCustomProviderAssociation -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="cc3ec-108">Opis</span><span class="sxs-lookup"><span data-stu-id="cc3ec-108">DESCRIPTION</span></span>
<span data-ttu-id="cc3ec-109">Uzyskaj powiązanie.</span><span class="sxs-lookup"><span data-stu-id="cc3ec-109">Get an association.</span></span>

## <span data-ttu-id="cc3ec-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cc3ec-110">EXAMPLES</span></span>

### <span data-ttu-id="cc3ec-111">Przykład 1: niestandardowa lista skojarzeń dostawców</span><span class="sxs-lookup"><span data-stu-id="cc3ec-111">Example 1: List custom provider associations</span></span>
```powershell
PS C:\> Get-AzCustomProviderAssociation

Location  Name             Type
--------  ----             ----
East US 2 MyAssoc   Microsoft.CustomProviders/associations
```

<span data-ttu-id="cc3ec-112">Lista wszystkich skojarzeń dostawców niestandardowych dla danego zakresu.</span><span class="sxs-lookup"><span data-stu-id="cc3ec-112">List all custom provider associations for a given scope.</span></span>

### <span data-ttu-id="cc3ec-113">Przykład 2: uzyskiwanie skojarzenia</span><span class="sxs-lookup"><span data-stu-id="cc3ec-113">Example 2: Get an association</span></span>
```powershell
PS C:\> Get-AzCustomProviderAssociation -Scope $resourceId -Name MyAssoc

Location  Name             Type
--------  ----             ----
East US 2 MyAssoc   Microsoft.CustomProviders/associations
```

<span data-ttu-id="cc3ec-114">Uzyskiwanie szczegółowych informacji o jednym skojarzeniu CustomProvider</span><span class="sxs-lookup"><span data-stu-id="cc3ec-114">Get details for a single CustomProvider association</span></span>

## <span data-ttu-id="cc3ec-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cc3ec-115">PARAMETERS</span></span>

### <span data-ttu-id="cc3ec-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc3ec-116">-DefaultProfile</span></span>
<span data-ttu-id="cc3ec-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cc3ec-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc3ec-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="cc3ec-118">-InputObject</span></span>
<span data-ttu-id="cc3ec-119">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="cc3ec-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="cc3ec-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cc3ec-120">-Name</span></span>
<span data-ttu-id="cc3ec-121">Nazwa skojarzenia.</span><span class="sxs-lookup"><span data-stu-id="cc3ec-121">The name of the association.</span></span>

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

### <span data-ttu-id="cc3ec-122">-Zakres</span><span class="sxs-lookup"><span data-stu-id="cc3ec-122">-Scope</span></span>
<span data-ttu-id="cc3ec-123">Zakres skojarzenia.</span><span class="sxs-lookup"><span data-stu-id="cc3ec-123">The scope of the association.</span></span>

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

### <span data-ttu-id="cc3ec-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc3ec-124">CommonParameters</span></span>
<span data-ttu-id="cc3ec-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc3ec-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc3ec-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cc3ec-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc3ec-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cc3ec-127">INPUTS</span></span>

### <span data-ttu-id="cc3ec-128">Microsoft. Azure. PowerShell. polecenia. CustomProviders. models. ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="cc3ec-128">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="cc3ec-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cc3ec-129">OUTPUTS</span></span>

### <span data-ttu-id="cc3ec-130">Microsoft. Azure. PowerShell. polecenia. CustomProviders. models. Api20180901Preview. IAssociation</span><span class="sxs-lookup"><span data-stu-id="cc3ec-130">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.IAssociation</span></span>

## <span data-ttu-id="cc3ec-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cc3ec-131">NOTES</span></span>

<span data-ttu-id="cc3ec-132">PISUJE</span><span class="sxs-lookup"><span data-stu-id="cc3ec-132">ALIASES</span></span>

<span data-ttu-id="cc3ec-133">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cc3ec-133">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cc3ec-134">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="cc3ec-134">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cc3ec-135">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cc3ec-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cc3ec-136">INPUTobject <ICustomProvidersIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="cc3ec-136">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cc3ec-137">`[AssociationName <String>]`: Nazwa skojarzenia.</span><span class="sxs-lookup"><span data-stu-id="cc3ec-137">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="cc3ec-138">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="cc3ec-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cc3ec-139">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cc3ec-139">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="cc3ec-140">`[ResourceProviderName <String>]`: Nazwa dostawcy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cc3ec-140">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="cc3ec-141">`[Scope <String>]`: Zakres skojarzenia.</span><span class="sxs-lookup"><span data-stu-id="cc3ec-141">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="cc3ec-142">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="cc3ec-142">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="cc3ec-143">Jest to ciąg sformatowany przy użyciu identyfikatora GUID (na przykład 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="cc3ec-143">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="cc3ec-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cc3ec-144">RELATED LINKS</span></span>

