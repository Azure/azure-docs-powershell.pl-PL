---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountgeneratedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountGeneratedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountGeneratedIcn.md
ms.openlocfilehash: 0dffb7a99e29ea4cc595cad1b5b92450e83289f4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220800"
---
# <span data-ttu-id="dc33e-101">Get-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="dc33e-101">Get-AzIntegrationAccountGeneratedIcn</span></span>

## <span data-ttu-id="dc33e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dc33e-102">SYNOPSIS</span></span>
<span data-ttu-id="dc33e-103">To polecenie cmdlet pobiera bieżącą wartość wygenerowanego numeru kontrolnego wymiany na umowę.</span><span class="sxs-lookup"><span data-stu-id="dc33e-103">This cmdlet retrieves the current value of the generated interchange control number per agreement.</span></span>

## <span data-ttu-id="dc33e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dc33e-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountGeneratedIcn -ResourceGroupName <String> -Name <String> [-AgreementName <String>]
 [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc33e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="dc33e-105">DESCRIPTION</span></span>
<span data-ttu-id="dc33e-106">To polecenie cmdlet jest przeznaczone do użycia w scenariuszach odzyskiwania po awarii w celu pobrania bieżącej wartości wygenerowanego numeru kontrolnego wymiany, tak aby można było zapisać zwiększoną wartość o wartości Set-AzIntegrationAccountGeneratedIcn.</span><span class="sxs-lookup"><span data-stu-id="dc33e-106">This cmdlet is meant to be used in disaster recovery scenarios to retrieve the current value of the generated interchange control number so to write back an increased value with Set-AzIntegrationAccountGeneratedIcn.</span></span>
<span data-ttu-id="dc33e-107">Numer kontrolki wymiany należy zwiększyć, aby uniknąć powielonych numerów kontrolnych wymiany dla liczb, które nie zostały jeszcze zreplikowane w regionie pasywnym, gdy wystąpił klęska żywiołowa w aktywnym regionie.</span><span class="sxs-lookup"><span data-stu-id="dc33e-107">The interchange control number should be increased to avoid duplicate interchange control numbers for the numbers that could not yet be replicated to the passive region when the disaster happened in the active region.</span></span>
<span data-ttu-id="dc33e-108">Podaj parametr "-Agreementtype", aby określić, czy numery kontrolek X12 lub EDIFACT mają być zwracane.</span><span class="sxs-lookup"><span data-stu-id="dc33e-108">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="dc33e-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dc33e-109">EXAMPLES</span></span>

### <span data-ttu-id="dc33e-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="dc33e-110">Example 1</span></span>
```
PS C:\> Get-AzIntegrationAccountGeneratedIcn -AgreementType "X12" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "X12IntegrationAccountAgreement"
ControlNumber            : 1000
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="dc33e-111">To polecenie umożliwia uzyskiwanie wygenerowanego numeru kontrolnego wymiany X12 z konta integracji według nazwy umowy.</span><span class="sxs-lookup"><span data-stu-id="dc33e-111">This command gets the integration account generated X12 interchange control number by agreement name.</span></span> <span data-ttu-id="dc33e-112">Upewnij się, że określona umowa jest typu "X12"</span><span class="sxs-lookup"><span data-stu-id="dc33e-112">Please make sure agreement specified is of type "X12"</span></span>

### <span data-ttu-id="dc33e-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="dc33e-113">Example 2</span></span>
```
PS C:\> Get-AzIntegrationAccountGeneratedIcn -AgreementType "Edifact" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "EdifactIntegrationAccountAgreement"
ControlNumber            : 1000
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="dc33e-114">To polecenie umożliwia uzyskiwanie wygenerowanego numeru kontrolnego wymiany EDIFACT z konta integracji według nazwy umowy.</span><span class="sxs-lookup"><span data-stu-id="dc33e-114">This command gets the integration account generated Edifact interchange control number by agreement name.</span></span> <span data-ttu-id="dc33e-115">Upewnij się, że określona umowa jest typu "EDIFACT"</span><span class="sxs-lookup"><span data-stu-id="dc33e-115">Please make sure agreement specified is of type "Edifact"</span></span>

### <span data-ttu-id="dc33e-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="dc33e-116">Example 3</span></span>
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

<span data-ttu-id="dc33e-117">To polecenie pobiera wszystkie wygenerowaną X12 numery kontrolne wymiany według nazwy konta integracji.</span><span class="sxs-lookup"><span data-stu-id="dc33e-117">This command gets all the generated X12 interchange control numbers by integration account name.</span></span>

## <span data-ttu-id="dc33e-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dc33e-118">PARAMETERS</span></span>

### <span data-ttu-id="dc33e-119">-Agreementname</span><span class="sxs-lookup"><span data-stu-id="dc33e-119">-AgreementName</span></span>
<span data-ttu-id="dc33e-120">Nazwa umowy dotyczącej konta integracji.</span><span class="sxs-lookup"><span data-stu-id="dc33e-120">The integration account agreement name.</span></span>

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

### <span data-ttu-id="dc33e-121">-Agreementtype</span><span class="sxs-lookup"><span data-stu-id="dc33e-121">-AgreementType</span></span>
<span data-ttu-id="dc33e-122">Typ umowy dotyczącej konta integracji.</span><span class="sxs-lookup"><span data-stu-id="dc33e-122">The integration account agreement type.</span></span>

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

### <span data-ttu-id="dc33e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc33e-123">-DefaultProfile</span></span>
<span data-ttu-id="dc33e-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="dc33e-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dc33e-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dc33e-125">-Name</span></span>
<span data-ttu-id="dc33e-126">Nazwa konta integracji.</span><span class="sxs-lookup"><span data-stu-id="dc33e-126">The integration account name.</span></span>

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

### <span data-ttu-id="dc33e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc33e-127">-ResourceGroupName</span></span>
<span data-ttu-id="dc33e-128">Nazwa grupy zasobów konta integracji.</span><span class="sxs-lookup"><span data-stu-id="dc33e-128">The integration account resource group name.</span></span>

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

### <span data-ttu-id="dc33e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc33e-129">CommonParameters</span></span>
<span data-ttu-id="dc33e-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc33e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc33e-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc33e-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc33e-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dc33e-132">INPUTS</span></span>

### <span data-ttu-id="dc33e-133">System. String</span><span class="sxs-lookup"><span data-stu-id="dc33e-133">System.String</span></span>

## <span data-ttu-id="dc33e-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dc33e-134">OUTPUTS</span></span>

### <span data-ttu-id="dc33e-135">Microsoft. Azure. Commands. LogicApp. Utilities. IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="dc33e-135">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="dc33e-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dc33e-136">NOTES</span></span>

## <span data-ttu-id="dc33e-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dc33e-137">RELATED LINKS</span></span>

[<span data-ttu-id="dc33e-138">Set-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="dc33e-138">Set-AzIntegrationAccountGeneratedIcn</span></span>](./Set-AzIntegrationAccountGeneratedIcn.md)

