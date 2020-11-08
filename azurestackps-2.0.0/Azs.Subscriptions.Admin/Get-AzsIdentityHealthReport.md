---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsidentityhealthreport
schema: 2.0.0
ms.openlocfilehash: 995ddf191f870fee9d27438ebea6d29729ca4c9f
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/22/2020
ms.locfileid: "94054099"
---
# <span data-ttu-id="13c23-101">Get-AzsIdentityHealthReport</span><span class="sxs-lookup"><span data-stu-id="13c23-101">Get-AzsIdentityHealthReport</span></span>

## <span data-ttu-id="13c23-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="13c23-102">SYNOPSIS</span></span>
<span data-ttu-id="13c23-103">Sprawdzanie kondycji tożsamości</span><span class="sxs-lookup"><span data-stu-id="13c23-103">Checks the identity health</span></span>

## <span data-ttu-id="13c23-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="13c23-104">SYNTAX</span></span>

### <span data-ttu-id="13c23-105">Zaznacz (domyślne)</span><span class="sxs-lookup"><span data-stu-id="13c23-105">Check (Default)</span></span>
```
Get-AzsIdentityHealthReport [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="13c23-106">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="13c23-106">CheckViaIdentity</span></span>
```
Get-AzsIdentityHealthReport -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="13c23-107">Opis</span><span class="sxs-lookup"><span data-stu-id="13c23-107">DESCRIPTION</span></span>
<span data-ttu-id="13c23-108">Sprawdzanie kondycji tożsamości</span><span class="sxs-lookup"><span data-stu-id="13c23-108">Checks the identity health</span></span>

## <span data-ttu-id="13c23-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="13c23-109">EXAMPLES</span></span>

### <span data-ttu-id="13c23-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="13c23-110">Example 1</span></span>
```powershell
PS C:\> Get-AzsIdentityHealthReport

ReportEndTimeUtc      ReportStartTimeUtc    Status 
----------------      ------------------    ------ 
3/12/2020 11:41:08 PM 3/12/2020 11:40:50 PM Healthy
```

<span data-ttu-id="13c23-111">Uzyskaj status kondycji tożsamości.</span><span class="sxs-lookup"><span data-stu-id="13c23-111">Get the status of the Identity Health.</span></span>

## <span data-ttu-id="13c23-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="13c23-112">PARAMETERS</span></span>

### <span data-ttu-id="13c23-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13c23-113">-DefaultProfile</span></span>
<span data-ttu-id="13c23-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="13c23-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13c23-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="13c23-115">-InputObject</span></span>
<span data-ttu-id="13c23-116">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="13c23-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: CheckViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="13c23-117">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="13c23-117">-SubscriptionId</span></span>
<span data-ttu-id="13c23-118">Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure. Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="13c23-118">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Check
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="13c23-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="13c23-119">-Confirm</span></span>
<span data-ttu-id="13c23-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13c23-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13c23-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13c23-121">-WhatIf</span></span>
<span data-ttu-id="13c23-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13c23-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13c23-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="13c23-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13c23-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13c23-124">CommonParameters</span></span>
<span data-ttu-id="13c23-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13c23-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13c23-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="13c23-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13c23-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="13c23-127">INPUTS</span></span>

### <span data-ttu-id="13c23-128">Microsoft. Azure. PowerShell. polecenia. SubscriptionsAdmin. models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="13c23-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="13c23-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="13c23-129">OUTPUTS</span></span>

### <span data-ttu-id="13c23-130">Microsoft. Azure. PowerShell. polecenia. SubscriptionsAdmin. models. Api20151101. IIdentityHealthCheckReportDefinition</span><span class="sxs-lookup"><span data-stu-id="13c23-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IIdentityHealthCheckReportDefinition</span></span>

<span data-ttu-id="13c23-131">PISUJE</span><span class="sxs-lookup"><span data-stu-id="13c23-131">ALIASES</span></span>

## <span data-ttu-id="13c23-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="13c23-132">NOTES</span></span>

<span data-ttu-id="13c23-133">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="13c23-133">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="13c23-134">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="13c23-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="13c23-135">INPUTobject <ISubscriptionsAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="13c23-135">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="13c23-136">`[DelegatedProvider <String>]`: DelegatedProvider identyfikator.</span><span class="sxs-lookup"><span data-stu-id="13c23-136">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="13c23-137">`[DelegatedProviderSubscriptionId <String>]`: Identyfikator subskrypcji delegowanego dostawcy.</span><span class="sxs-lookup"><span data-stu-id="13c23-137">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="13c23-138">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="13c23-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="13c23-139">`[Location <String>]`: Lokalizacja AzureStack.</span><span class="sxs-lookup"><span data-stu-id="13c23-139">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="13c23-140">`[ManifestName <String>]`: Nazwa manifestu.</span><span class="sxs-lookup"><span data-stu-id="13c23-140">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="13c23-141">`[Offer <String>]`: Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="13c23-141">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="13c23-142">`[OfferDelegationName <String>]`: Nazwa delegowania oferty.</span><span class="sxs-lookup"><span data-stu-id="13c23-142">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="13c23-143">`[OperationsStatusName <String>]`: Nazwa stanu operacji.</span><span class="sxs-lookup"><span data-stu-id="13c23-143">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="13c23-144">`[Plan <String>]`: Nazwa planu.</span><span class="sxs-lookup"><span data-stu-id="13c23-144">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="13c23-145">`[PlanAcquisitionId <String>]`: Identyfikator nabycie planu</span><span class="sxs-lookup"><span data-stu-id="13c23-145">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="13c23-146">`[Quota <String>]`: Nazwa przydziału.</span><span class="sxs-lookup"><span data-stu-id="13c23-146">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="13c23-147">`[ResourceGroupName <String>]`: Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="13c23-147">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="13c23-148">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure. Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="13c23-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="13c23-149">`[TargetSubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="13c23-149">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="13c23-150">`[Tenant <String>]`: Nazwa dzierżawy katalogu.</span><span class="sxs-lookup"><span data-stu-id="13c23-150">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="13c23-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="13c23-151">RELATED LINKS</span></span>

