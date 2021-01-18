---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/invoke-azcostmanagementexecuteexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Invoke-AzCostManagementExecuteExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Invoke-AzCostManagementExecuteExport.md
ms.openlocfilehash: 752af43a72151296c4c90ecc32923a786c7b4081
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503767"
---
# <span data-ttu-id="eb213-101">Invoke-AzCostManagementExecuteExport</span><span class="sxs-lookup"><span data-stu-id="eb213-101">Invoke-AzCostManagementExecuteExport</span></span>

## <span data-ttu-id="eb213-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="eb213-102">SYNOPSIS</span></span>
<span data-ttu-id="eb213-103">Operacja wykonania operacji eksportowania.</span><span class="sxs-lookup"><span data-stu-id="eb213-103">The operation to execute an export.</span></span>

## <span data-ttu-id="eb213-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="eb213-104">SYNTAX</span></span>

### <span data-ttu-id="eb213-105">Wykonywanie (domyślne)</span><span class="sxs-lookup"><span data-stu-id="eb213-105">Execute (Default)</span></span>
```
Invoke-AzCostManagementExecuteExport -ExportName <String> -Scope <String> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="eb213-106">ExecuteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="eb213-106">ExecuteViaIdentity</span></span>
```
Invoke-AzCostManagementExecuteExport -InputObject <ICostManagementIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="eb213-107">Opis</span><span class="sxs-lookup"><span data-stu-id="eb213-107">DESCRIPTION</span></span>
<span data-ttu-id="eb213-108">Operacja wykonania operacji eksportowania.</span><span class="sxs-lookup"><span data-stu-id="eb213-108">The operation to execute an export.</span></span>

## <span data-ttu-id="eb213-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="eb213-109">EXAMPLES</span></span>

### <span data-ttu-id="eb213-110">Przykład 1: wywoływanie eksportu przez Eksportname i zakres</span><span class="sxs-lookup"><span data-stu-id="eb213-110">Example 1: Invoke Export by ExportName and Scope</span></span>
```powershell
PS C:\> Invoke-AzCostManagementExecuteExport -ExportName 'TestExport' -Scope 'subscriptions/**********'

```

<span data-ttu-id="eb213-111">Wywoływanie eksportu za pomocą Eksportuname i zakresu</span><span class="sxs-lookup"><span data-stu-id="eb213-111">Invoke Export by ExportName and Scope</span></span>

### <span data-ttu-id="eb213-112">Przykład 2: wywoływanie operacji eksportowania przezobject</span><span class="sxs-lookup"><span data-stu-id="eb213-112">Example 2: Invoke Export by InputObject</span></span>
```powershell
PS C:\> $getExport = Get-AzCostManagementExport -Name 'TestExport' -Scope 'subscriptions/**********'
Invoke-AzCostManagementExecuteExport -InputObject $getExport

```

<span data-ttu-id="eb213-113">Wywoływanie operacji eksportowania przez wejście</span><span class="sxs-lookup"><span data-stu-id="eb213-113">Invoke Export by InputObject</span></span>

## <span data-ttu-id="eb213-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="eb213-114">PARAMETERS</span></span>

### <span data-ttu-id="eb213-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb213-115">-DefaultProfile</span></span>
<span data-ttu-id="eb213-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="eb213-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb213-117">-Exportname</span><span class="sxs-lookup"><span data-stu-id="eb213-117">-ExportName</span></span>
<span data-ttu-id="eb213-118">Eksportuj nazwę.</span><span class="sxs-lookup"><span data-stu-id="eb213-118">Export Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Execute
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb213-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="eb213-119">-InputObject</span></span>
<span data-ttu-id="eb213-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="eb213-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity
Parameter Sets: ExecuteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eb213-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eb213-121">-PassThru</span></span>
<span data-ttu-id="eb213-122">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="eb213-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="eb213-123">-Zakres</span><span class="sxs-lookup"><span data-stu-id="eb213-123">-Scope</span></span>
<span data-ttu-id="eb213-124">Ten parametr definiuje zakres costmanagement z różnych perspektyw "abonament", "Resources" i "świadczenie usługi".</span><span class="sxs-lookup"><span data-stu-id="eb213-124">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

```yaml
Type: System.String
Parameter Sets: Execute
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb213-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="eb213-125">-Confirm</span></span>
<span data-ttu-id="eb213-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb213-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb213-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb213-127">-WhatIf</span></span>
<span data-ttu-id="eb213-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb213-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb213-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="eb213-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb213-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb213-130">CommonParameters</span></span>
<span data-ttu-id="eb213-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb213-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb213-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eb213-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb213-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eb213-133">INPUTS</span></span>

### <span data-ttu-id="eb213-134">Microsoft. Azure. PowerShell. polecenia. CostManagement. models. ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="eb213-134">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="eb213-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="eb213-135">OUTPUTS</span></span>

### <span data-ttu-id="eb213-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="eb213-136">System.Boolean</span></span>

## <span data-ttu-id="eb213-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="eb213-137">NOTES</span></span>

<span data-ttu-id="eb213-138">PISUJE</span><span class="sxs-lookup"><span data-stu-id="eb213-138">ALIASES</span></span>

<span data-ttu-id="eb213-139">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="eb213-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="eb213-140">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="eb213-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="eb213-141">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="eb213-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="eb213-142">INPUTobject <ICostManagementIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="eb213-142">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="eb213-143">`[AlertId <String>]`: Identyfikator alertu</span><span class="sxs-lookup"><span data-stu-id="eb213-143">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="eb213-144">`[ExportName <String>]`: Nazwa eksportu.</span><span class="sxs-lookup"><span data-stu-id="eb213-144">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="eb213-145">`[ExternalCloudProviderId <String>]`: Może to być "{externalSubscriptionId}" dla połączonego konta lub "{externalBillingAccountId}" dla konta skonsolidowanego, które jest używane z operacjami wymiaru/kwerendy.</span><span class="sxs-lookup"><span data-stu-id="eb213-145">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="eb213-146">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: Typ zewnętrznego dostawcy chmury skojarzony z operacjami wymiaru/kwerendy.</span><span class="sxs-lookup"><span data-stu-id="eb213-146">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="eb213-147">Obejmuje to "externalSubscriptions" dla połączonego konta, a także "externalBillingAccounts" dla konta skonsolidowanego.</span><span class="sxs-lookup"><span data-stu-id="eb213-147">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="eb213-148">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="eb213-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="eb213-149">`[Scope <String>]`: Zakres skojarzony z operacjami wyświetlania.</span><span class="sxs-lookup"><span data-stu-id="eb213-149">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="eb213-150">Obejmuje to "abonament/{subskrypcji}" dla zakresu abonamentu, "abonaments/{Binding}/resourceGroups/{resourceGroupName}" dla zakresu grupy zasobów. Providers/Microsoft. rozliczenia/billingAccounts/{billingAccountId} "dla zakresu kont rozliczeniowych" Providers/Microsoft. rozliczenia/billingAccounts/{billingAccountId}/działy/{departmentId} "dla zakresu działu," Providers/Microsoft. rozliczenia/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId} "dla zakresu EnrollmentAccount," Providers/Microsoft. rozliczenia/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId} "dla zakresu BillingProfile," Providers/Microsoft. rozliczenia/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId} "dla zakresu InvoiceSection," Providers/Microsoft. Management/managementGroups/{managementGroupId} ' dla zakresu grupy zarządzania, "Providers/Microsoft. CostManagement/externalBillingAccounts/{externalBillingAccountName}" dla zewnętrznego zakresu konta rozliczeniowego i "Providers/Microsoft. CostManagement/externalSubscriptions/{externalSubscriptionName}" dla zakresu subskrypcji zewnętrznej.</span><span class="sxs-lookup"><span data-stu-id="eb213-150">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="eb213-151">`[ViewName <String>]`: Nazwa widoku</span><span class="sxs-lookup"><span data-stu-id="eb213-151">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="eb213-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eb213-152">RELATED LINKS</span></span>

