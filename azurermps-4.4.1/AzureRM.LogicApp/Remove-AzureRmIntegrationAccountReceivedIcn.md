---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountReceivedIcn.md
ms.openlocfilehash: 95c2b33b52ed9660c57aad35128af4eba277c0a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550944"
---
# <span data-ttu-id="c1723-101">Remove-AzureRmIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="c1723-101">Remove-AzureRmIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="c1723-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c1723-102">SYNOPSIS</span></span>
<span data-ttu-id="c1723-103">To polecenie cmdlet umożliwia usunięcie konkretnego otrzymanego numeru kontrolnego wymiany według umowy i wartości numeru sterującego.</span><span class="sxs-lookup"><span data-stu-id="c1723-103">This cmdlet removes a specific received interchange control number per agreement and control number value.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1723-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c1723-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1723-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c1723-105">DESCRIPTION</span></span>
<span data-ttu-id="c1723-106">To polecenie cmdlet jest używane w scenariuszach odzyskiwania po awarii, aby usunąć odebrany numer kontrolki wymiany z konta integracji, tak aby łącznik B2B mógł ponownie przetworzyć komunikat po włączeniu wykrywania zduplikowanych liczb.</span><span class="sxs-lookup"><span data-stu-id="c1723-106">This cmdlet is meant to be used in disaster recovery scenarios to remove a received interchange control number from the integration account so that the B2B connector may process again the message when duplicate number detection is enabled.</span></span>
<span data-ttu-id="c1723-107">Rzadko zdarza się, że otrzymany numer kontrolki wymiany może być rezerwowany tuż przed katastrofą, a łącznik B2B odrzuca transliczbę jako błędną.</span><span class="sxs-lookup"><span data-stu-id="c1723-107">In rare occasions the received interchange control number may be reserved shortly before a disaster and before the B2B connector rejects the interchange as erroneous.</span></span>
<span data-ttu-id="c1723-108">W takim przypadku operacja może wymagać ponownego przetworzenia witryny odzyskiwania po skorygowaniu jej ładunku.</span><span class="sxs-lookup"><span data-stu-id="c1723-108">In such occasions the operation may want to enable the recovery site to process again the same interchange after its payload is corrected.</span></span>
<span data-ttu-id="c1723-109">Podaj parametr "-Agreementtype", aby określić, czy numery kontrolek X12 lub EDIFACT mają być zwracane.</span><span class="sxs-lookup"><span data-stu-id="c1723-109">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="c1723-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c1723-110">EXAMPLES</span></span>

### <span data-ttu-id="c1723-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c1723-111">Example 1</span></span>
```
PS C:\> Get-AzureRmIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
Get-AzureRmIntegrationAccountReceivedIcn : The existing recevied control number '000000641' for agreement 'X12AgreementName' is not in a valid format.
At line:1 char:1
+ Get-AzureRmIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzureRmIntegrationAccountReceivedIcn], PSInvalidOperationException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand

PS C:\> Remove-AzureRmIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
PS C:\> Get-AzureRmIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
Get-AzureRmIntegrationAccountReceivedIcn : The session 'X12-ICN-X12AgreementName-000000641' could not be found in integration account 'accountName'.
At line:1 char:1
+ Get-AzureRmIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzureRmIntegrationAccountReceivedIcn], CloudException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand
```

<span data-ttu-id="c1723-112">Próbuje uzyskać otrzymany numer kontrolki wymiany X12, którego format zawartości jest nieprawidłowy.</span><span class="sxs-lookup"><span data-stu-id="c1723-112">Attempts to get a received X12 interchange control number which content is not in a valid format.</span></span>
<span data-ttu-id="c1723-113">Usuwa otrzymany numer kontrolki wymiany X12.</span><span class="sxs-lookup"><span data-stu-id="c1723-113">Removes the received X12 interchange control number.</span></span>
<span data-ttu-id="c1723-114">Potwierdza, że otrzymany numer kontrolki wymiany X12 został usunięty, próbując go ponownie pobrać.</span><span class="sxs-lookup"><span data-stu-id="c1723-114">Confirms the received X12 interchange control number was removed by attempting to get it again.</span></span>

### <span data-ttu-id="c1723-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="c1723-115">Example 2</span></span>
```
PS C:\> Get-AzureRmIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
Get-AzureRmIntegrationAccountReceivedIcn : The existing recevied control number '000000641' for agreement 'EdifactAgreementName' is not in a valid format.
At line:1 char:1
+ Get-AzureRmIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzureRmIntegrationAccountReceivedIcn], PSInvalidOperationException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand

PS C:\> Remove-AzureRmIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
PS C:\> Get-AzureRmIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
Get-AzureRmIntegrationAccountReceivedIcn : The session 'Edifact-ICN-EdifactAgreementName-000000641' could not be found in integration account 'accountName'.
At line:1 char:1
+ Get-AzureRmIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzureRmIntegrationAccountReceivedIcn], CloudException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand
```

<span data-ttu-id="c1723-116">Próbuje uzyskać otrzymany numer kontrolki wymiany EDIFACT, którego format zawartości jest nieprawidłowy.</span><span class="sxs-lookup"><span data-stu-id="c1723-116">Attempts to get a received Edifact interchange control number which content is not in a valid format.</span></span>
<span data-ttu-id="c1723-117">Usuwa otrzymany numer kontrolki wymiany EDIFACT.</span><span class="sxs-lookup"><span data-stu-id="c1723-117">Removes the received Edifact interchange control number.</span></span>
<span data-ttu-id="c1723-118">Potwierdza, że otrzymany numer kontrolki wymiany EDIFACT został usunięty, próbując go ponownie pobrać.</span><span class="sxs-lookup"><span data-stu-id="c1723-118">Confirms the received Edifact interchange control number was removed by attempting to get it again.</span></span>

## <span data-ttu-id="c1723-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c1723-119">PARAMETERS</span></span>

### <span data-ttu-id="c1723-120">-Agreementname</span><span class="sxs-lookup"><span data-stu-id="c1723-120">-AgreementName</span></span>
<span data-ttu-id="c1723-121">Nazwa umowy dotyczącej konta integracji.</span><span class="sxs-lookup"><span data-stu-id="c1723-121">The integration account agreement name.</span></span>

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

### <span data-ttu-id="c1723-122">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="c1723-122">-ControlNumberValue</span></span>
<span data-ttu-id="c1723-123">Wartość numeru kontrolnego konta integracji.</span><span class="sxs-lookup"><span data-stu-id="c1723-123">The integration account control number value.</span></span>

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

### <span data-ttu-id="c1723-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c1723-124">-Name</span></span>
<span data-ttu-id="c1723-125">Nazwa konta integracji.</span><span class="sxs-lookup"><span data-stu-id="c1723-125">The integration account name.</span></span>

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

### <span data-ttu-id="c1723-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1723-126">-ResourceGroupName</span></span>
<span data-ttu-id="c1723-127">Nazwa grupy zasobów konta integracji.</span><span class="sxs-lookup"><span data-stu-id="c1723-127">The integration account resource group name.</span></span>

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

### <span data-ttu-id="c1723-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c1723-128">-Confirm</span></span>
<span data-ttu-id="c1723-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1723-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1723-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1723-130">-WhatIf</span></span>
<span data-ttu-id="c1723-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1723-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1723-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c1723-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1723-133">-Agreementtype</span><span class="sxs-lookup"><span data-stu-id="c1723-133">-AgreementType</span></span>
<span data-ttu-id="c1723-134">Typ umowy dotyczącej konta integracji.</span><span class="sxs-lookup"><span data-stu-id="c1723-134">The integration account agreement type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MessageType

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1723-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1723-135">-DefaultProfile</span></span>
<span data-ttu-id="c1723-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c1723-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1723-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1723-137">CommonParameters</span></span>
<span data-ttu-id="c1723-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1723-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1723-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1723-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1723-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c1723-140">INPUTS</span></span>

### <span data-ttu-id="c1723-141">System. String</span><span class="sxs-lookup"><span data-stu-id="c1723-141">System.String</span></span>

## <span data-ttu-id="c1723-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c1723-142">OUTPUTS</span></span>

### <span data-ttu-id="c1723-143">System. Object</span><span class="sxs-lookup"><span data-stu-id="c1723-143">System.Object</span></span>

## <span data-ttu-id="c1723-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c1723-144">NOTES</span></span>

## <span data-ttu-id="c1723-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c1723-145">RELATED LINKS</span></span>

<span data-ttu-id="c1723-146">[Get-AzureRmIntegrationAccountReceivedIcn](./Get-AzureRmIntegrationAccountReceivedIcn.md) 
 [Set-AzureRmIntegrationAccountReceivedIcn](./Set-AzureRmIntegrationAccountReceivedIcn.md)</span><span class="sxs-lookup"><span data-stu-id="c1723-146">[Get-AzureRmIntegrationAccountReceivedIcn](./Get-AzureRmIntegrationAccountReceivedIcn.md)
[Set-AzureRmIntegrationAccountReceivedIcn](./Set-AzureRmIntegrationAccountReceivedIcn.md)</span></span>

