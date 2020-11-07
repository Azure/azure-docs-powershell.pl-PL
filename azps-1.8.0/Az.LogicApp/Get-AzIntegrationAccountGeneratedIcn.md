---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountgeneratedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountGeneratedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountGeneratedIcn.md
ms.openlocfilehash: 971e96b61b22bd5efbd22b82468d864a63392a16
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867747"
---
# <span data-ttu-id="e7e2b-101">Get-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="e7e2b-101">Get-AzIntegrationAccountGeneratedIcn</span></span>

## <span data-ttu-id="e7e2b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e7e2b-102">SYNOPSIS</span></span>
<span data-ttu-id="e7e2b-103">To polecenie cmdlet pobiera bieżącą wartość wygenerowanego numeru kontrolnego wymiany na umowę.</span><span class="sxs-lookup"><span data-stu-id="e7e2b-103">This cmdlet retrieves the current value of the generated interchange control number per agreement.</span></span>

## <span data-ttu-id="e7e2b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e7e2b-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountGeneratedIcn -ResourceGroupName <String> -Name <String> [-AgreementName <String>]
 [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7e2b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e7e2b-105">DESCRIPTION</span></span>
<span data-ttu-id="e7e2b-106">To polecenie cmdlet jest przeznaczone do użycia w scenariuszach odzyskiwania po awarii w celu pobrania bieżącej wartości wygenerowanego numeru kontrolnego wymiany, tak aby można było zapisać zwiększoną wartość o wartości Set-AzIntegrationAccountGeneratedIcn.</span><span class="sxs-lookup"><span data-stu-id="e7e2b-106">This cmdlet is meant to be used in disaster recovery scenarios to retrieve the current value of the generated interchange control number so to write back an increased value with Set-AzIntegrationAccountGeneratedIcn.</span></span>
<span data-ttu-id="e7e2b-107">Numer kontrolki wymiany należy zwiększyć, aby uniknąć powielonych numerów kontrolnych wymiany dla liczb, które nie zostały jeszcze zreplikowane w regionie pasywnym, gdy wystąpił klęska żywiołowa w aktywnym regionie.</span><span class="sxs-lookup"><span data-stu-id="e7e2b-107">The interchange control number should be increased to avoid duplicate interchange control numbers for the numbers that could not yet be replicated to the passive region when the disaster happened in the active region.</span></span>
<span data-ttu-id="e7e2b-108">Podaj parametr "-Agreementtype", aby określić, czy numery kontrolek X12 lub EDIFACT mają być zwracane.</span><span class="sxs-lookup"><span data-stu-id="e7e2b-108">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="e7e2b-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e7e2b-109">EXAMPLES</span></span>

### <span data-ttu-id="e7e2b-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e7e2b-110">Example 1</span></span>
```
PS C:\> Get-AzIntegrationAccountGeneratedIcn -AgreementType "X12" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "X12IntegrationAccountAgreement"
ControlNumber            : 1000
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="e7e2b-111">To polecenie umożliwia uzyskiwanie wygenerowanego numeru kontrolnego wymiany X12 z konta integracji według nazwy umowy.</span><span class="sxs-lookup"><span data-stu-id="e7e2b-111">This command gets the integration account generated X12 interchange control number by agreement name.</span></span> <span data-ttu-id="e7e2b-112">Upewnij się, że określona umowa jest typu "X12"</span><span class="sxs-lookup"><span data-stu-id="e7e2b-112">Please make sure agreement specified is of type "X12"</span></span>

### <span data-ttu-id="e7e2b-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e7e2b-113">Example 2</span></span>
```
PS C:\> Get-AzIntegrationAccountGeneratedIcn -AgreementType "Edifact" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "EdifactIntegrationAccountAgreement"
ControlNumber            : 1000
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="e7e2b-114">To polecenie umożliwia uzyskiwanie wygenerowanego numeru kontrolnego wymiany EDIFACT z konta integracji według nazwy umowy.</span><span class="sxs-lookup"><span data-stu-id="e7e2b-114">This command gets the integration account generated Edifact interchange control number by agreement name.</span></span> <span data-ttu-id="e7e2b-115">Upewnij się, że określona umowa jest typu "EDIFACT"</span><span class="sxs-lookup"><span data-stu-id="e7e2b-115">Please make sure agreement specified is of type "Edifact"</span></span>

### <span data-ttu-id="e7e2b-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="e7e2b-116">Example 3</span></span>
```
PS C:\> Get-AzIntegrationAccountGeneratedIcn -AgreementType "X12" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1"
ControlNumber            : 1000
ControlNumberChangedTime : 2/22/2017 8:05:41 PM
AgreementName            : X12IntegrationAccountAgreement1
IsMessageProcessingFailed:

ControlNumber            : 1000
ControlNumberChangedTime : 2/22/2017 8:05:41 PM
AgreementName            : X12IntegrationAccountAgreement2
IsMessageProcessingFailed:

ControlNumber            : No generated control number was found for this agreement.
ControlNumberChangedTime : 1/1/0001 12:00:00 AM
AgreementName            : X12IntegrationAccountAgreement3
IsMessageProcessingFailed:
```

<span data-ttu-id="e7e2b-117">To polecenie pobiera wszystkie wygenerowaną X12 numery kontrolne wymiany według nazwy konta integracji.</span><span class="sxs-lookup"><span data-stu-id="e7e2b-117">This command gets all the generated X12 interchange control numbers by integration account name.</span></span>

## <span data-ttu-id="e7e2b-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e7e2b-118">PARAMETERS</span></span>

### <span data-ttu-id="e7e2b-119">-Agreementname</span><span class="sxs-lookup"><span data-stu-id="e7e2b-119">-AgreementName</span></span>
<span data-ttu-id="e7e2b-120">Nazwa umowy dotyczącej konta integracji.</span><span class="sxs-lookup"><span data-stu-id="e7e2b-120">The integration account agreement name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7e2b-121">-Agreementtype</span><span class="sxs-lookup"><span data-stu-id="e7e2b-121">-AgreementType</span></span>
<span data-ttu-id="e7e2b-122">Typ umowy dotyczącej konta integracji.</span><span class="sxs-lookup"><span data-stu-id="e7e2b-122">The integration account agreement type.</span></span>

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

### <span data-ttu-id="e7e2b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7e2b-123">-DefaultProfile</span></span>
<span data-ttu-id="e7e2b-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e7e2b-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e7e2b-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e7e2b-125">-Name</span></span>
<span data-ttu-id="e7e2b-126">Nazwa konta integracji.</span><span class="sxs-lookup"><span data-stu-id="e7e2b-126">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7e2b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7e2b-127">-ResourceGroupName</span></span>
<span data-ttu-id="e7e2b-128">Nazwa grupy zasobów konta integracji.</span><span class="sxs-lookup"><span data-stu-id="e7e2b-128">The integration account resource group name.</span></span>

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

### <span data-ttu-id="e7e2b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7e2b-129">CommonParameters</span></span>
<span data-ttu-id="e7e2b-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7e2b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7e2b-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7e2b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7e2b-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e7e2b-132">INPUTS</span></span>

### <span data-ttu-id="e7e2b-133">System. String</span><span class="sxs-lookup"><span data-stu-id="e7e2b-133">System.String</span></span>

## <span data-ttu-id="e7e2b-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e7e2b-134">OUTPUTS</span></span>

### <span data-ttu-id="e7e2b-135">Microsoft. Azure. Commands. LogicApp. Utilities. IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="e7e2b-135">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="e7e2b-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e7e2b-136">NOTES</span></span>

## <span data-ttu-id="e7e2b-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e7e2b-137">RELATED LINKS</span></span>

[<span data-ttu-id="e7e2b-138">Set-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="e7e2b-138">Set-AzIntegrationAccountGeneratedIcn</span></span>](./Set-AzIntegrationAccountGeneratedIcn.md)

