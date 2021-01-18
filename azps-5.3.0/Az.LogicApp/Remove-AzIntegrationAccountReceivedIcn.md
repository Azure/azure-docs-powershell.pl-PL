---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountReceivedIcn.md
ms.openlocfilehash: 2a80173900c0faf062c3d4ba0c0a3b2029737bcf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98500838"
---
# <span data-ttu-id="8dae5-101">Remove-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="8dae5-101">Remove-AzIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="8dae5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8dae5-102">SYNOPSIS</span></span>
<span data-ttu-id="8dae5-103">To polecenie cmdlet umożliwia usunięcie konkretnego otrzymanego numeru kontrolnego wymiany według umowy i wartości numeru sterującego.</span><span class="sxs-lookup"><span data-stu-id="8dae5-103">This cmdlet removes a specific received interchange control number per agreement and control number value.</span></span>

## <span data-ttu-id="8dae5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8dae5-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8dae5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8dae5-105">DESCRIPTION</span></span>
<span data-ttu-id="8dae5-106">To polecenie cmdlet jest używane w scenariuszach odzyskiwania po awarii, aby usunąć odebrany numer kontrolki wymiany z konta integracji, tak aby łącznik B2B mógł ponownie przetworzyć komunikat po włączeniu wykrywania zduplikowanych liczb.</span><span class="sxs-lookup"><span data-stu-id="8dae5-106">This cmdlet is meant to be used in disaster recovery scenarios to remove a received interchange control number from the integration account so that the B2B connector may process again the message when duplicate number detection is enabled.</span></span>
<span data-ttu-id="8dae5-107">Rzadko zdarza się, że otrzymany numer kontrolki wymiany może być rezerwowany tuż przed katastrofą, a łącznik B2B odrzuca transliczbę jako błędną.</span><span class="sxs-lookup"><span data-stu-id="8dae5-107">In rare occasions the received interchange control number may be reserved shortly before a disaster and before the B2B connector rejects the interchange as erroneous.</span></span>
<span data-ttu-id="8dae5-108">W takim przypadku operacja może wymagać ponownego przetworzenia witryny odzyskiwania po skorygowaniu jej ładunku.</span><span class="sxs-lookup"><span data-stu-id="8dae5-108">In such occasions the operation may want to enable the recovery site to process again the same interchange after its payload is corrected.</span></span>
<span data-ttu-id="8dae5-109">Podaj parametr "-Agreementtype", aby określić, czy numery kontrolek X12 lub EDIFACT mają być zwracane.</span><span class="sxs-lookup"><span data-stu-id="8dae5-109">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="8dae5-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8dae5-110">EXAMPLES</span></span>

### <span data-ttu-id="8dae5-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8dae5-111">Example 1</span></span>
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

<span data-ttu-id="8dae5-112">Próbuje uzyskać otrzymany numer kontrolki wymiany X12, którego format zawartości jest nieprawidłowy.</span><span class="sxs-lookup"><span data-stu-id="8dae5-112">Attempts to get a received X12 interchange control number which content is not in a valid format.</span></span>
<span data-ttu-id="8dae5-113">Usuwa otrzymany numer kontrolki wymiany X12.</span><span class="sxs-lookup"><span data-stu-id="8dae5-113">Removes the received X12 interchange control number.</span></span>
<span data-ttu-id="8dae5-114">Potwierdza, że otrzymany numer kontrolki wymiany X12 został usunięty, próbując go ponownie pobrać.</span><span class="sxs-lookup"><span data-stu-id="8dae5-114">Confirms the received X12 interchange control number was removed by attempting to get it again.</span></span>

### <span data-ttu-id="8dae5-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="8dae5-115">Example 2</span></span>
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

<span data-ttu-id="8dae5-116">Próbuje uzyskać otrzymany numer kontrolki wymiany EDIFACT, którego format zawartości jest nieprawidłowy.</span><span class="sxs-lookup"><span data-stu-id="8dae5-116">Attempts to get a received Edifact interchange control number which content is not in a valid format.</span></span>
<span data-ttu-id="8dae5-117">Usuwa otrzymany numer kontrolki wymiany EDIFACT.</span><span class="sxs-lookup"><span data-stu-id="8dae5-117">Removes the received Edifact interchange control number.</span></span>
<span data-ttu-id="8dae5-118">Potwierdza, że otrzymany numer kontrolki wymiany EDIFACT został usunięty, próbując go ponownie pobrać.</span><span class="sxs-lookup"><span data-stu-id="8dae5-118">Confirms the received Edifact interchange control number was removed by attempting to get it again.</span></span>

## <span data-ttu-id="8dae5-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8dae5-119">PARAMETERS</span></span>

### <span data-ttu-id="8dae5-120">-Agreementname</span><span class="sxs-lookup"><span data-stu-id="8dae5-120">-AgreementName</span></span>
<span data-ttu-id="8dae5-121">Nazwa umowy dotyczącej konta integracji.</span><span class="sxs-lookup"><span data-stu-id="8dae5-121">The integration account agreement name.</span></span>

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

### <span data-ttu-id="8dae5-122">-Agreementtype</span><span class="sxs-lookup"><span data-stu-id="8dae5-122">-AgreementType</span></span>
<span data-ttu-id="8dae5-123">Typ umowy dotyczącej konta integracji.</span><span class="sxs-lookup"><span data-stu-id="8dae5-123">The integration account agreement type.</span></span>

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

### <span data-ttu-id="8dae5-124">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="8dae5-124">-ControlNumberValue</span></span>
<span data-ttu-id="8dae5-125">Wartość numeru kontrolnego konta integracji.</span><span class="sxs-lookup"><span data-stu-id="8dae5-125">The integration account control number value.</span></span>

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

### <span data-ttu-id="8dae5-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dae5-126">-DefaultProfile</span></span>
<span data-ttu-id="8dae5-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="8dae5-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8dae5-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8dae5-128">-Name</span></span>
<span data-ttu-id="8dae5-129">Nazwa konta integracji.</span><span class="sxs-lookup"><span data-stu-id="8dae5-129">The integration account name.</span></span>

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

### <span data-ttu-id="8dae5-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8dae5-130">-ResourceGroupName</span></span>
<span data-ttu-id="8dae5-131">Nazwa grupy zasobów konta integracji.</span><span class="sxs-lookup"><span data-stu-id="8dae5-131">The integration account resource group name.</span></span>

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

### <span data-ttu-id="8dae5-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8dae5-132">-Confirm</span></span>
<span data-ttu-id="8dae5-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8dae5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8dae5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8dae5-134">-WhatIf</span></span>
<span data-ttu-id="8dae5-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8dae5-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8dae5-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8dae5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8dae5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dae5-137">CommonParameters</span></span>
<span data-ttu-id="8dae5-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8dae5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dae5-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8dae5-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dae5-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8dae5-140">INPUTS</span></span>

### <span data-ttu-id="8dae5-141">System. String</span><span class="sxs-lookup"><span data-stu-id="8dae5-141">System.String</span></span>

## <span data-ttu-id="8dae5-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8dae5-142">OUTPUTS</span></span>

### <span data-ttu-id="8dae5-143">System. void</span><span class="sxs-lookup"><span data-stu-id="8dae5-143">System.Void</span></span>

## <span data-ttu-id="8dae5-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8dae5-144">NOTES</span></span>

## <span data-ttu-id="8dae5-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8dae5-145">RELATED LINKS</span></span>

<span data-ttu-id="8dae5-146">[Get-AzIntegrationAccountReceivedIcn](./Get-AzIntegrationAccountReceivedIcn.md) 
 [Set-AzIntegrationAccountReceivedIcn](./Set-AzIntegrationAccountReceivedIcn.md)</span><span class="sxs-lookup"><span data-stu-id="8dae5-146">[Get-AzIntegrationAccountReceivedIcn](./Get-AzIntegrationAccountReceivedIcn.md)
[Set-AzIntegrationAccountReceivedIcn](./Set-AzIntegrationAccountReceivedIcn.md)</span></span>

