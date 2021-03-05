---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/powershell/module/az.logicapp/remove-azintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountReceivedIcn.md
ms.openlocfilehash: a87ccecbba21479c24a2defd2d7443f66184a799
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961930"
---
# <span data-ttu-id="d359b-101">Remove-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="d359b-101">Remove-AzIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="d359b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d359b-102">SYNOPSIS</span></span>
<span data-ttu-id="d359b-103">To polecenie cmdlet usuwa określony otrzymany numer kontroli interchange na umowę i wartość numeru kontrolki.</span><span class="sxs-lookup"><span data-stu-id="d359b-103">This cmdlet removes a specific received interchange control number per agreement and control number value.</span></span>

## <span data-ttu-id="d359b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d359b-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d359b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d359b-105">DESCRIPTION</span></span>
<span data-ttu-id="d359b-106">To polecenie cmdlet jest przeznaczone do użycia w scenariuszach odzyskiwania po awarii w celu usunięcia otrzymanego numeru kontroli wymiany z konta integracji, dzięki czemu łącznik B2B może ponownie przetworzyć ten komunikat, gdy jest włączone wykrywanie zduplikowanych liczb.</span><span class="sxs-lookup"><span data-stu-id="d359b-106">This cmdlet is meant to be used in disaster recovery scenarios to remove a received interchange control number from the integration account so that the B2B connector may process again the message when duplicate number detection is enabled.</span></span>
<span data-ttu-id="d359b-107">W rzadkich przypadkach otrzymany numer kontroli wymiany może być zarezerwowany na krótko przed awarią i przed odrzuceniem łącznika B2B jako błędnego.</span><span class="sxs-lookup"><span data-stu-id="d359b-107">In rare occasions the received interchange control number may be reserved shortly before a disaster and before the B2B connector rejects the interchange as erroneous.</span></span>
<span data-ttu-id="d359b-108">W takich przypadkach operacja może wymagać umożliwienia witrynie odzyskiwania przetwarzania ponownie tej samej wymiany po poprawioniu jej obciążenia.</span><span class="sxs-lookup"><span data-stu-id="d359b-108">In such occasions the operation may want to enable the recovery site to process again the same interchange after its payload is corrected.</span></span>
<span data-ttu-id="d359b-109">Podaj parametr "-AgreementType", aby określić, czy mają być zwracane numery kontrolek X12, czy Edifact.</span><span class="sxs-lookup"><span data-stu-id="d359b-109">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="d359b-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d359b-110">EXAMPLES</span></span>

### <span data-ttu-id="d359b-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d359b-111">Example 1</span></span>
```
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
Get-AzIntegrationAccountReceivedIcn : The existing received control number '000000641' for agreement 'X12AgreementName' is not in a valid format.
At line:1 char:1
+ Get-AzIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzIntegrationAccountReceivedIcn], PSInvalidOperationException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand

PS C:\> Remove-AzIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
Get-AzIntegrationAccountReceivedIcn : The session 'X12-ICN-X12AgreementName-000000641' could not be found in integration account 'accountName'.
At line:1 char:1
+ Get-AzIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzIntegrationAccountReceivedIcn], CloudException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand
```

<span data-ttu-id="d359b-112">Próbuje uzyskać otrzymany numer kontrolki wymiany X12, którego zawartość nie ma prawidłowego formatu.</span><span class="sxs-lookup"><span data-stu-id="d359b-112">Attempts to get a received X12 interchange control number which content is not in a valid format.</span></span>
<span data-ttu-id="d359b-113">Usuwa otrzymany numer kontrolki wymiany X12.</span><span class="sxs-lookup"><span data-stu-id="d359b-113">Removes the received X12 interchange control number.</span></span>
<span data-ttu-id="d359b-114">Potwierdza, że odebrany numer wymiany X12 został usunięty, próbując go ponownie pobrać.</span><span class="sxs-lookup"><span data-stu-id="d359b-114">Confirms the received X12 interchange control number was removed by attempting to get it again.</span></span>

### <span data-ttu-id="d359b-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d359b-115">Example 2</span></span>
```
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
Get-AzIntegrationAccountReceivedIcn : The existing received control number '000000641' for agreement 'EdifactAgreementName' is not in a valid format.
At line:1 char:1
+ Get-AzIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzIntegrationAccountReceivedIcn], PSInvalidOperationException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand

PS C:\> Remove-AzIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
Get-AzIntegrationAccountReceivedIcn : The session 'Edifact-ICN-EdifactAgreementName-000000641' could not be found in integration account 'accountName'.
At line:1 char:1
+ Get-AzIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzIntegrationAccountReceivedIcn], CloudException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand
```

<span data-ttu-id="d359b-116">Próbuje uzyskać otrzymany numer wymiany Edifact, który zawartość nie ma prawidłowego formatu.</span><span class="sxs-lookup"><span data-stu-id="d359b-116">Attempts to get a received Edifact interchange control number which content is not in a valid format.</span></span>
<span data-ttu-id="d359b-117">Usuwa otrzymany numer wymiany Edifact.</span><span class="sxs-lookup"><span data-stu-id="d359b-117">Removes the received Edifact interchange control number.</span></span>
<span data-ttu-id="d359b-118">Potwierdza, że odebrany numer wymiany Edifact został usunięty, próbując go ponownie pobrać.</span><span class="sxs-lookup"><span data-stu-id="d359b-118">Confirms the received Edifact interchange control number was removed by attempting to get it again.</span></span>

## <span data-ttu-id="d359b-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d359b-119">PARAMETERS</span></span>

### <span data-ttu-id="d359b-120">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="d359b-120">-AgreementName</span></span>
<span data-ttu-id="d359b-121">Nazwa umowy konta integracji.</span><span class="sxs-lookup"><span data-stu-id="d359b-121">The integration account agreement name.</span></span>

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

### <span data-ttu-id="d359b-122">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="d359b-122">-AgreementType</span></span>
<span data-ttu-id="d359b-123">Typ umowy konta integracji.</span><span class="sxs-lookup"><span data-stu-id="d359b-123">The integration account agreement type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MessageType
Accepted values: X12, Edifact

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d359b-124">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="d359b-124">-ControlNumberValue</span></span>
<span data-ttu-id="d359b-125">Wartość numeru kontrolki konta integracji.</span><span class="sxs-lookup"><span data-stu-id="d359b-125">The integration account control number value.</span></span>

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

### <span data-ttu-id="d359b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d359b-126">-DefaultProfile</span></span>
<span data-ttu-id="d359b-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="d359b-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d359b-128">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d359b-128">-Name</span></span>
<span data-ttu-id="d359b-129">Nazwa konta integracji.</span><span class="sxs-lookup"><span data-stu-id="d359b-129">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d359b-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d359b-130">-ResourceGroupName</span></span>
<span data-ttu-id="d359b-131">Nazwa grupy zasobów konta integracji.</span><span class="sxs-lookup"><span data-stu-id="d359b-131">The integration account resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d359b-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d359b-132">-Confirm</span></span>
<span data-ttu-id="d359b-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d359b-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d359b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d359b-134">-WhatIf</span></span>
<span data-ttu-id="d359b-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d359b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d359b-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d359b-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d359b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d359b-137">CommonParameters</span></span>
<span data-ttu-id="d359b-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d359b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d359b-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d359b-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d359b-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d359b-140">INPUTS</span></span>

### <span data-ttu-id="d359b-141">System.String</span><span class="sxs-lookup"><span data-stu-id="d359b-141">System.String</span></span>

## <span data-ttu-id="d359b-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d359b-142">OUTPUTS</span></span>

### <span data-ttu-id="d359b-143">System.Void</span><span class="sxs-lookup"><span data-stu-id="d359b-143">System.Void</span></span>

## <span data-ttu-id="d359b-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d359b-144">NOTES</span></span>

## <span data-ttu-id="d359b-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d359b-145">RELATED LINKS</span></span>

<span data-ttu-id="d359b-146">[Get-AzIntegrationAccountReceivedIcn](./Get-AzIntegrationAccountReceivedIcn.md) 
 [Set-AzIntegrationAccountReceivedIcn](./Set-AzIntegrationAccountReceivedIcn.md)</span><span class="sxs-lookup"><span data-stu-id="d359b-146">[Get-AzIntegrationAccountReceivedIcn](./Get-AzIntegrationAccountReceivedIcn.md)
[Set-AzIntegrationAccountReceivedIcn](./Set-AzIntegrationAccountReceivedIcn.md)</span></span>

