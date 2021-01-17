---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/get-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStore.md
ms.openlocfilehash: 88847cbb128f5545a235eb2c5c02043231ff1078
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381502"
---
# <span data-ttu-id="6b148-101">Get-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="6b148-101">Get-AzAppConfigurationStore</span></span>

## <span data-ttu-id="6b148-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6b148-102">SYNOPSIS</span></span>
<span data-ttu-id="6b148-103">Pobierz lub Wyświetl magazyny konfiguracji aplikacji.</span><span class="sxs-lookup"><span data-stu-id="6b148-103">Get or list app configuration stores.</span></span>

## <span data-ttu-id="6b148-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6b148-104">SYNTAX</span></span>

### <span data-ttu-id="6b148-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="6b148-105">List (Default)</span></span>
```
Get-AzAppConfigurationStore [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6b148-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="6b148-106">Get</span></span>
```
Get-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6b148-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6b148-107">GetViaIdentity</span></span>
```
Get-AzAppConfigurationStore -InputObject <IAppConfigurationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="6b148-108">List1</span><span class="sxs-lookup"><span data-stu-id="6b148-108">List1</span></span>
```
Get-AzAppConfigurationStore -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="6b148-109">Opis</span><span class="sxs-lookup"><span data-stu-id="6b148-109">DESCRIPTION</span></span>
<span data-ttu-id="6b148-110">Pobierz lub Wyświetl magazyny konfiguracji aplikacji.</span><span class="sxs-lookup"><span data-stu-id="6b148-110">Get or list app configuration stores.</span></span>

## <span data-ttu-id="6b148-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6b148-111">EXAMPLES</span></span>

### <span data-ttu-id="6b148-112">Przykład 1: wyświetlanie wszystkich magazynów konfiguracji aplikacji w ramach abonamentu</span><span class="sxs-lookup"><span data-stu-id="6b148-112">Example 1: List all app configuration stores under a subscription</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore

Location Name               Type
-------- ----               ----
eastus   appconfig-test01   Microsoft.AppConfiguration/configurationStores
eastus   contoso-app-config Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="6b148-113">To polecenie wyświetla listę wszystkich magazynów konfiguracji aplikacji w ramach abonamentu.</span><span class="sxs-lookup"><span data-stu-id="6b148-113">This command lists all app configuration stores under a subscription.</span></span>

### <span data-ttu-id="6b148-114">Przykład 2: Lista wszystkich magazynów konfiguracji aplikacji w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="6b148-114">Example 2: List all app configuration stores under a resource group</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
eastus   appconfig-test02 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="6b148-115">To polecenie wyświetla listę wszystkich magazynów konfiguracji aplikacji w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="6b148-115">This command lists all app configuration stores under a resource group.</span></span>

### <span data-ttu-id="6b148-116">Przykład 3: uzyskiwanie magazynu konfiguracji aplikacji według nazwy</span><span class="sxs-lookup"><span data-stu-id="6b148-116">Example 3: Get an app configuration store by name</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test01

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="6b148-117">To polecenie pobiera magazyn konfiguracji aplikacji według nazwy.</span><span class="sxs-lookup"><span data-stu-id="6b148-117">This command gets an app configuration store by name.</span></span>

### <span data-ttu-id="6b148-118">Przykład 4: uzyskiwanie magazynu konfiguracji aplikacji według rurociągu</span><span class="sxs-lookup"><span data-stu-id="6b148-118">Example 4: Get an app configuration store by pipeline</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test01 | Get-AzAppConfigurationStore

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="6b148-119">To polecenie pobiera magazyn konfiguracji aplikacji według rurociągu.</span><span class="sxs-lookup"><span data-stu-id="6b148-119">This command gets an app configuration store by pipeline.</span></span>

## <span data-ttu-id="6b148-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6b148-120">PARAMETERS</span></span>

### <span data-ttu-id="6b148-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b148-121">-DefaultProfile</span></span>
<span data-ttu-id="6b148-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6b148-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b148-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6b148-123">-InputObject</span></span>
<span data-ttu-id="6b148-124">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="6b148-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b148-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6b148-125">-Name</span></span>
<span data-ttu-id="6b148-126">Nazwa magazynu konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="6b148-126">The name of the configuration store.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b148-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b148-127">-ResourceGroupName</span></span>
<span data-ttu-id="6b148-128">Nazwa grupy zasobów, do której należy rejestr kontenera.</span><span class="sxs-lookup"><span data-stu-id="6b148-128">The name of the resource group to which the container registry belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b148-129">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="6b148-129">-SubscriptionId</span></span>
<span data-ttu-id="6b148-130">Identyfikator subskrypcji platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6b148-130">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="6b148-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b148-131">CommonParameters</span></span>
<span data-ttu-id="6b148-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b148-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b148-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6b148-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b148-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6b148-134">INPUTS</span></span>

### <span data-ttu-id="6b148-135">Microsoft. Azure. PowerShell. polecenia. AppConfiguration. models. IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="6b148-135">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="6b148-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6b148-136">OUTPUTS</span></span>

### <span data-ttu-id="6b148-137">Microsoft. Azure. PowerShell. polecenia. AppConfiguration. models. Api20200601. IConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="6b148-137">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span></span>

## <span data-ttu-id="6b148-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6b148-138">NOTES</span></span>

<span data-ttu-id="6b148-139">PISUJE</span><span class="sxs-lookup"><span data-stu-id="6b148-139">ALIASES</span></span>

<span data-ttu-id="6b148-140">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6b148-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6b148-141">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="6b148-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6b148-142">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6b148-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6b148-143">INPUTobject <IAppConfigurationIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="6b148-143">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6b148-144">`[ConfigStoreName <String>]`: Nazwa magazynu konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="6b148-144">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="6b148-145">`[GroupName <String>]`: Nazwa grupy zasobów linku prywatnego.</span><span class="sxs-lookup"><span data-stu-id="6b148-145">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="6b148-146">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="6b148-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6b148-147">`[PrivateEndpointConnectionName <String>]`: Nazwa połączenia prywatnego punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="6b148-147">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="6b148-148">`[ResourceGroupName <String>]`: Nazwa grupy zasobów, do której należy rejestr kontenera.</span><span class="sxs-lookup"><span data-stu-id="6b148-148">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="6b148-149">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6b148-149">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="6b148-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6b148-150">RELATED LINKS</span></span>

