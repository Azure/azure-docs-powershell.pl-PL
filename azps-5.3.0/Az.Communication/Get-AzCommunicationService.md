---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/get-azcommunicationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Get-AzCommunicationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Get-AzCommunicationService.md
ms.openlocfilehash: 3101ca2b120860dfa6df95786e235fc88fd0fc78
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504171"
---
# <span data-ttu-id="df4d1-101">Get-AzCommunicationService</span><span class="sxs-lookup"><span data-stu-id="df4d1-101">Get-AzCommunicationService</span></span>

## <span data-ttu-id="df4d1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="df4d1-102">SYNOPSIS</span></span>
<span data-ttu-id="df4d1-103">Pobierz CommunicationService i jej właściwości.</span><span class="sxs-lookup"><span data-stu-id="df4d1-103">Get the CommunicationService and its properties.</span></span>

## <span data-ttu-id="df4d1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="df4d1-104">SYNTAX</span></span>

### <span data-ttu-id="df4d1-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="df4d1-105">List (Default)</span></span>
```
Get-AzCommunicationService [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="df4d1-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="df4d1-106">Get</span></span>
```
Get-AzCommunicationService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="df4d1-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="df4d1-107">GetViaIdentity</span></span>
```
Get-AzCommunicationService -InputObject <ICommunicationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="df4d1-108">List1</span><span class="sxs-lookup"><span data-stu-id="df4d1-108">List1</span></span>
```
Get-AzCommunicationService -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="df4d1-109">Opis</span><span class="sxs-lookup"><span data-stu-id="df4d1-109">DESCRIPTION</span></span>
<span data-ttu-id="df4d1-110">Pobierz CommunicationService i jej właściwości.</span><span class="sxs-lookup"><span data-stu-id="df4d1-110">Get the CommunicationService and its properties.</span></span>

## <span data-ttu-id="df4d1-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="df4d1-111">EXAMPLES</span></span>

### <span data-ttu-id="df4d1-112">Przykład 1: Lista istniejących CommunicationServices dla subskrypcji</span><span class="sxs-lookup"><span data-stu-id="df4d1-112">Example 1: List existing CommunicationServices for a Subscription</span></span>
```powershell
PS C:\> Get-AzCommunicationService -SubscriptionId 73fc3592-3cef-4300-5e19-8d18b65ce0e8

Location Name             Type                                          AzureAsyncOperation
-------- ----             ----                                          -------------------
global   ContosoResource1   Microsoft.Communication/communicationServices
global   ContosoResource4   Microsoft.Communication/communicationServices
global   ContosoResource3   Microsoft.Communication/communicationServices
global   ContosoResource5   Microsoft.Communication/communicationServices
```

<span data-ttu-id="df4d1-113">Zwraca listę wszystkich zasobów ACS w ramach tego abonamentu.</span><span class="sxs-lookup"><span data-stu-id="df4d1-113">Returns a list of all ACS resources under that subscription.</span></span>

### <span data-ttu-id="df4d1-114">Przykład 2: uzyskiwanie informacji o określonym zasobie komunikacyjnej platformy Azure</span><span class="sxs-lookup"><span data-stu-id="df4d1-114">Example 2: Get infomation on specified Azure Communication resource</span></span>
```powershell
PS C:\> Get-AzCommunicationService -Name ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1

Location Name           Type                                          AzureAsyncOperation
-------- ----           ----                                          -------------------
Global   ContosoAcsResource1 Microsoft.Communication/communicationServices
```

<span data-ttu-id="df4d1-115">Zwraca informacje dotyczące zasobu ACS, jeśli znaleziono jedno pasujące podane parametry.</span><span class="sxs-lookup"><span data-stu-id="df4d1-115">Returns the information on an ACS resource, if one matching provided parameters is found.</span></span>

## <span data-ttu-id="df4d1-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="df4d1-116">PARAMETERS</span></span>

### <span data-ttu-id="df4d1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df4d1-117">-DefaultProfile</span></span>
<span data-ttu-id="df4d1-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="df4d1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df4d1-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="df4d1-119">-InputObject</span></span>
<span data-ttu-id="df4d1-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="df4d1-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df4d1-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="df4d1-121">-Name</span></span>
<span data-ttu-id="df4d1-122">Nazwa zasobu CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="df4d1-122">The name of the CommunicationService resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: CommunicationServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df4d1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df4d1-123">-ResourceGroupName</span></span>
<span data-ttu-id="df4d1-124">Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="df4d1-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="df4d1-125">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="df4d1-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="df4d1-126">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="df4d1-126">-SubscriptionId</span></span>
<span data-ttu-id="df4d1-127">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="df4d1-127">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="df4d1-128">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="df4d1-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="df4d1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df4d1-129">CommonParameters</span></span>
<span data-ttu-id="df4d1-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df4d1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df4d1-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="df4d1-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df4d1-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="df4d1-132">INPUTS</span></span>

### <span data-ttu-id="df4d1-133">Microsoft. Azure. PowerShell. cmdlet. Communication. models. ICommunicationIdentity</span><span class="sxs-lookup"><span data-stu-id="df4d1-133">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span></span>

## <span data-ttu-id="df4d1-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="df4d1-134">OUTPUTS</span></span>

### <span data-ttu-id="df4d1-135">Microsoft. Azure. PowerShell. cmdlet. Communication. models. Api20200820Preview. ICommunicationServiceResource</span><span class="sxs-lookup"><span data-stu-id="df4d1-135">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span></span>

## <span data-ttu-id="df4d1-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="df4d1-136">NOTES</span></span>

<span data-ttu-id="df4d1-137">PISUJE</span><span class="sxs-lookup"><span data-stu-id="df4d1-137">ALIASES</span></span>

<span data-ttu-id="df4d1-138">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="df4d1-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="df4d1-139">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="df4d1-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="df4d1-140">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="df4d1-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="df4d1-141">INPUTobject <ICommunicationIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="df4d1-141">INPUTOBJECT <ICommunicationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="df4d1-142">`[CommunicationServiceName <String>]`: Nazwa zasobu CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="df4d1-142">`[CommunicationServiceName <String>]`: The name of the CommunicationService resource.</span></span>
  - <span data-ttu-id="df4d1-143">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="df4d1-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="df4d1-144">`[Location <String>]`: Region platformy Azure</span><span class="sxs-lookup"><span data-stu-id="df4d1-144">`[Location <String>]`: The Azure region</span></span>
  - <span data-ttu-id="df4d1-145">`[OperationId <String>]`: Identyfikator trwającej operacji asynchronicznej</span><span class="sxs-lookup"><span data-stu-id="df4d1-145">`[OperationId <String>]`: The ID of an ongoing async operation</span></span>
  - <span data-ttu-id="df4d1-146">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="df4d1-146">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="df4d1-147">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="df4d1-147">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="df4d1-148">`[SubscriptionId <String>]`: Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="df4d1-148">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="df4d1-149">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="df4d1-149">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="df4d1-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="df4d1-150">RELATED LINKS</span></span>

