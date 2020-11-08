---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/get-azsapmonitorproviderinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitorProviderInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitorProviderInstance.md
ms.openlocfilehash: 55ca24a7213dea4e9d0743689c080ebbb439430a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222348"
---
# <span data-ttu-id="f6b46-101">Get-AzSapMonitorProviderInstance</span><span class="sxs-lookup"><span data-stu-id="f6b46-101">Get-AzSapMonitorProviderInstance</span></span>

## <span data-ttu-id="f6b46-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f6b46-102">SYNOPSIS</span></span>
<span data-ttu-id="f6b46-103">Pobiera właściwości wystąpienia dostawcy dotyczące określonego abonamentu, grupy zasobów, nazwy SapMonitor i nazwy zasobu.</span><span class="sxs-lookup"><span data-stu-id="f6b46-103">Gets properties of a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="f6b46-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f6b46-104">SYNTAX</span></span>

### <span data-ttu-id="f6b46-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="f6b46-105">List (Default)</span></span>
```
Get-AzSapMonitorProviderInstance -ResourceGroupName <String> -SapMonitorName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f6b46-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="f6b46-106">Get</span></span>
```
Get-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f6b46-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f6b46-107">GetViaIdentity</span></span>
```
Get-AzSapMonitorProviderInstance -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="f6b46-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f6b46-108">DESCRIPTION</span></span>
<span data-ttu-id="f6b46-109">Pobiera właściwości wystąpienia dostawcy dotyczące określonego abonamentu, grupy zasobów, nazwy SapMonitor i nazwy zasobu.</span><span class="sxs-lookup"><span data-stu-id="f6b46-109">Gets properties of a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="f6b46-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f6b46-110">EXAMPLES</span></span>

### <span data-ttu-id="f6b46-111">Przykład 1. Pobierz wszystkie wystąpienia na monitorze SAP</span><span class="sxs-lookup"><span data-stu-id="f6b46-111">Example 1: Get all instances under a SAP monitor</span></span>
```powershell
PS C:\> Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01

Name                 Type
----                 ----
ps-sapmonitorins-t01 Microsoft.HanaOnAzure/sapMonitors/providerInstances
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="f6b46-112">To polecenie pobiera wszystkie wystąpienia pod monitorem SAP.</span><span class="sxs-lookup"><span data-stu-id="f6b46-112">This command gets all instances under a SAP monitor.</span></span>

### <span data-ttu-id="f6b46-113">Przykład 2: uzyskiwanie wystąpień monitora SAP według nazwy</span><span class="sxs-lookup"><span data-stu-id="f6b46-113">Example 2: Get an instances of SAP monitor by name</span></span>
```powershell
PS C:\> Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t02

Name                 Type
----                 ----
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="f6b46-114">To polecenie pobiera wystąpienia monitora protokołu SAP według nazwy.</span><span class="sxs-lookup"><span data-stu-id="f6b46-114">This command gets an instances of SAP monitor by name.</span></span>

### <span data-ttu-id="f6b46-115">Przykład 3: uzyskiwanie wystąpień monitora protokołu SAP według obiektów</span><span class="sxs-lookup"><span data-stu-id="f6b46-115">Example 3: Get an instances of SAP monitor by object</span></span>
```powershell
PS C:\> $sapIns = Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t02
PS C:\> Get-AzSapMonitorProviderInstance -InputObject $sapIns

Name                 Type
----                 ----
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="f6b46-116">To polecenie pobiera wystąpienia monitora protokołu SAP według obiektu.</span><span class="sxs-lookup"><span data-stu-id="f6b46-116">This command gets an instances of SAP monitor by object.</span></span>

### <span data-ttu-id="f6b46-117">Przykład 4: uzyskiwanie wystąpień monitora protokołu SAP według rurociągu</span><span class="sxs-lookup"><span data-stu-id="f6b46-117">Example 4: Get an instances of SAP monitor by pipeline</span></span>
```powershell
PS C:\> @{Id = "/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/nancyc-hn1/providers/Microsoft.HanaOnAzure/sapMonitors/ps-spamonitor-t01/providerInstances/ps-sapmonitorins-t02"} | Get-AzSapMonitorProviderInstance

Name                 Type
----                 ----
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="f6b46-118">To polecenie pobiera wystąpienia monitora protokołu SAP według rurociągu.</span><span class="sxs-lookup"><span data-stu-id="f6b46-118">This command gets an instances of SAP monitor by pipeline.</span></span>

## <span data-ttu-id="f6b46-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f6b46-119">PARAMETERS</span></span>

### <span data-ttu-id="f6b46-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6b46-120">-DefaultProfile</span></span>
<span data-ttu-id="f6b46-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f6b46-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6b46-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f6b46-122">-InputObject</span></span>
<span data-ttu-id="f6b46-123">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="f6b46-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6b46-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f6b46-124">-Name</span></span>
<span data-ttu-id="f6b46-125">Nazwa wystąpienia dostawcy.</span><span class="sxs-lookup"><span data-stu-id="f6b46-125">Name of the provider instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ProviderInstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6b46-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6b46-126">-ResourceGroupName</span></span>
<span data-ttu-id="f6b46-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f6b46-127">Name of the resource group.</span></span>

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

### <span data-ttu-id="f6b46-128">-SapMonitorName</span><span class="sxs-lookup"><span data-stu-id="f6b46-128">-SapMonitorName</span></span>
<span data-ttu-id="f6b46-129">Nazwa zasobu monitorowania protokołu SAP.</span><span class="sxs-lookup"><span data-stu-id="f6b46-129">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="f6b46-130">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="f6b46-130">-SubscriptionId</span></span>
<span data-ttu-id="f6b46-131">Identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f6b46-131">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f6b46-132">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="f6b46-132">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6b46-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6b46-133">CommonParameters</span></span>
<span data-ttu-id="f6b46-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6b46-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6b46-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f6b46-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6b46-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f6b46-136">INPUTS</span></span>

### <span data-ttu-id="f6b46-137">Microsoft. Azure. PowerShell. polecenia. HanaOnAzure. models. IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="f6b46-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="f6b46-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f6b46-138">OUTPUTS</span></span>

### <span data-ttu-id="f6b46-139">Microsoft. Azure. PowerShell. polecenia. HanaOnAzure. models. Api20200207Preview. IProviderInstance</span><span class="sxs-lookup"><span data-stu-id="f6b46-139">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.IProviderInstance</span></span>

## <span data-ttu-id="f6b46-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f6b46-140">NOTES</span></span>

<span data-ttu-id="f6b46-141">PISUJE</span><span class="sxs-lookup"><span data-stu-id="f6b46-141">ALIASES</span></span>

<span data-ttu-id="f6b46-142">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f6b46-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f6b46-143">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="f6b46-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f6b46-144">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f6b46-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f6b46-145">INPUTobject <IHanaOnAzureIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="f6b46-145">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f6b46-146">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="f6b46-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f6b46-147">`[Location <String>]`: Lokalizacja usuniętego magazynu.</span><span class="sxs-lookup"><span data-stu-id="f6b46-147">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="f6b46-148">`[OperationKind <AccessPolicyUpdateKind?>]`: Nazwa operacji</span><span class="sxs-lookup"><span data-stu-id="f6b46-148">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="f6b46-149">`[ProviderInstanceName <String>]`: Nazwa wystąpienia dostawcy.</span><span class="sxs-lookup"><span data-stu-id="f6b46-149">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="f6b46-150">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f6b46-150">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="f6b46-151">`[ResourceName <String>]`: Nazwa zasobu tożsamości.</span><span class="sxs-lookup"><span data-stu-id="f6b46-151">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="f6b46-152">`[SapMonitorName <String>]`: Nazwa zasobu monitora SAP.</span><span class="sxs-lookup"><span data-stu-id="f6b46-152">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="f6b46-153">`[Scope <String>]`: Zakres zasobu dostawca zasobów.</span><span class="sxs-lookup"><span data-stu-id="f6b46-153">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="f6b46-154">Zasób nadrzędny jest rozszerzany przez zarządzane tożsamości.</span><span class="sxs-lookup"><span data-stu-id="f6b46-154">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="f6b46-155">`[SubscriptionId <String>]`: Identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f6b46-155">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f6b46-156">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="f6b46-156">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="f6b46-157">`[VaultName <String>]`: Nazwa magazynu</span><span class="sxs-lookup"><span data-stu-id="f6b46-157">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="f6b46-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f6b46-158">RELATED LINKS</span></span>

