---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/get-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProvider.md
ms.openlocfilehash: 42b4059b146a752980b1067272713bf0a22c2c46
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94306709"
---
# <span data-ttu-id="045a5-101">Get-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="045a5-101">Get-AzCustomProvider</span></span>

## <span data-ttu-id="045a5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="045a5-102">SYNOPSIS</span></span>
<span data-ttu-id="045a5-103">Pobiera manifest dostawcy zasobów niestandardowych.</span><span class="sxs-lookup"><span data-stu-id="045a5-103">Gets the custom resource provider manifest.</span></span>

## <span data-ttu-id="045a5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="045a5-104">SYNTAX</span></span>

### <span data-ttu-id="045a5-105">List1 (domyślny)</span><span class="sxs-lookup"><span data-stu-id="045a5-105">List1 (Default)</span></span>
```
Get-AzCustomProvider [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="045a5-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="045a5-106">Get</span></span>
```
Get-AzCustomProvider -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="045a5-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="045a5-107">GetViaIdentity</span></span>
```
Get-AzCustomProvider -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="045a5-108">Lista</span><span class="sxs-lookup"><span data-stu-id="045a5-108">List</span></span>
```
Get-AzCustomProvider -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="045a5-109">Opis</span><span class="sxs-lookup"><span data-stu-id="045a5-109">DESCRIPTION</span></span>
<span data-ttu-id="045a5-110">Pobiera manifest dostawcy zasobów niestandardowych.</span><span class="sxs-lookup"><span data-stu-id="045a5-110">Gets the custom resource provider manifest.</span></span>

## <span data-ttu-id="045a5-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="045a5-111">EXAMPLES</span></span>

### <span data-ttu-id="045a5-112">Przykład 1: wyświetlanie wszystkich dostawców niestandardowych w ramach subskrypcji</span><span class="sxs-lookup"><span data-stu-id="045a5-112">Example 1: List all Custom Providers in a subscription</span></span>
```powershell
PS C:\> Get-AzCustomProvider

Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
East US 2 Namespace2.Type  Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="045a5-113">Wyświetla listę wszystkich dostawców niestandardowych w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="045a5-113">Lists all the custom providers in a subscription</span></span>

### <span data-ttu-id="045a5-114">Przykład 2: uzyskiwanie jednego dostawcy niestandardowego</span><span class="sxs-lookup"><span data-stu-id="045a5-114">Example 2: Get a single custom provider</span></span>
```powershell
PS C:\> Get-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type | Format-List

Action            :
Id                : /subscriptions/xxxxx-yyyyy-xxxx-yyyy/resourceGroups/mc-cp01/providers/Microsoft.CustomProviders/resourceproviders/Namespace.Type
Location          : West US 2
Name              : Namespace.Type
ProvisioningState : Succeeded
ResourceType      : {CustomRoute1, associations}
Tag               : Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ResourceTags
Type              : Microsoft.CustomProviders/resourceproviders
Validation        :

```

<span data-ttu-id="045a5-115">Pobiera szczegóły dla jednego dostawcy niestandardowego.</span><span class="sxs-lookup"><span data-stu-id="045a5-115">Gets details for a single custom provider.</span></span>
<span data-ttu-id="045a5-116">Użyj Format-List, aby wyświetlić szczegóły obiektu na ekranie.</span><span class="sxs-lookup"><span data-stu-id="045a5-116">Use Format-List to show object details on the screen.</span></span>

## <span data-ttu-id="045a5-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="045a5-117">PARAMETERS</span></span>

### <span data-ttu-id="045a5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="045a5-118">-DefaultProfile</span></span>
<span data-ttu-id="045a5-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="045a5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="045a5-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="045a5-120">-InputObject</span></span>
<span data-ttu-id="045a5-121">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="045a5-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="045a5-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="045a5-122">-Name</span></span>
<span data-ttu-id="045a5-123">Nazwa dostawcy zasobów.</span><span class="sxs-lookup"><span data-stu-id="045a5-123">The name of the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ResourceProviderName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="045a5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="045a5-124">-ResourceGroupName</span></span>
<span data-ttu-id="045a5-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="045a5-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="045a5-126">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="045a5-126">-SubscriptionId</span></span>
<span data-ttu-id="045a5-127">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="045a5-127">The Azure subscription ID.</span></span>
<span data-ttu-id="045a5-128">Jest to ciąg sformatowany przy użyciu identyfikatora GUID (na przykład 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="045a5-128">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="045a5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="045a5-129">CommonParameters</span></span>
<span data-ttu-id="045a5-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="045a5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="045a5-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="045a5-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="045a5-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="045a5-132">INPUTS</span></span>

### <span data-ttu-id="045a5-133">Microsoft. Azure. PowerShell. polecenia. CustomProviders. models. ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="045a5-133">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="045a5-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="045a5-134">OUTPUTS</span></span>

### <span data-ttu-id="045a5-135">Microsoft. Azure. PowerShell. polecenia. CustomProviders. models. Api20180901Preview. ICustomRpManifest</span><span class="sxs-lookup"><span data-stu-id="045a5-135">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span></span>

## <span data-ttu-id="045a5-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="045a5-136">NOTES</span></span>

<span data-ttu-id="045a5-137">PISUJE</span><span class="sxs-lookup"><span data-stu-id="045a5-137">ALIASES</span></span>

<span data-ttu-id="045a5-138">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="045a5-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="045a5-139">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="045a5-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="045a5-140">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="045a5-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="045a5-141">INPUTobject <ICustomProvidersIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="045a5-141">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="045a5-142">`[AssociationName <String>]`: Nazwa skojarzenia.</span><span class="sxs-lookup"><span data-stu-id="045a5-142">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="045a5-143">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="045a5-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="045a5-144">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="045a5-144">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="045a5-145">`[ResourceProviderName <String>]`: Nazwa dostawcy zasobów.</span><span class="sxs-lookup"><span data-stu-id="045a5-145">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="045a5-146">`[Scope <String>]`: Zakres skojarzenia.</span><span class="sxs-lookup"><span data-stu-id="045a5-146">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="045a5-147">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="045a5-147">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="045a5-148">Jest to ciąg sformatowany przy użyciu identyfikatora GUID (na przykład 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="045a5-148">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="045a5-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="045a5-149">RELATED LINKS</span></span>

