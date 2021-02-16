---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountgeneratedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountGeneratedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountGeneratedIcn.md
ms.openlocfilehash: 0dffb7a99e29ea4cc595cad1b5b92450e83289f4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180394"
---
# <span data-ttu-id="88885-101">Get-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="88885-101">Get-AzIntegrationAccountGeneratedIcn</span></span>

## <span data-ttu-id="88885-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88885-102">SYNOPSIS</span></span>
<span data-ttu-id="88885-103">To polecenie cmdlet pobiera bieżącą wartość wygenerowanego numeru kontrolki wymiany na umowę.</span><span class="sxs-lookup"><span data-stu-id="88885-103">This cmdlet retrieves the current value of the generated interchange control number per agreement.</span></span>

## <span data-ttu-id="88885-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="88885-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountGeneratedIcn -ResourceGroupName <String> -Name <String> [-AgreementName <String>]
 [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88885-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="88885-105">DESCRIPTION</span></span>
<span data-ttu-id="88885-106">To polecenie cmdlet jest przeznaczone do użycia w scenariuszach odzyskiwania po awarii w celu pobrania bieżącej wartości wygenerowanego numeru kontrolki wymiany w celu odpisania zwiększonej wartości za pomocą polecenia Set-AzIntegrationAccountGeneratedIcn.</span><span class="sxs-lookup"><span data-stu-id="88885-106">This cmdlet is meant to be used in disaster recovery scenarios to retrieve the current value of the generated interchange control number so to write back an increased value with Set-AzIntegrationAccountGeneratedIcn.</span></span>
<span data-ttu-id="88885-107">Należy zwiększyć numer kontroli wymiany, aby uniknąć zduplikowanych numerów kontroli wymiany dla numerów, których nie można było jeszcze zreplikować do regionu pasywnego w przypadku awarii w aktywnym regionie.</span><span class="sxs-lookup"><span data-stu-id="88885-107">The interchange control number should be increased to avoid duplicate interchange control numbers for the numbers that could not yet be replicated to the passive region when the disaster happened in the active region.</span></span>
<span data-ttu-id="88885-108">Podaj parametr "-AgreementType", aby określić, czy mają być zwracane numery kontrolek X12, czy Edifact.</span><span class="sxs-lookup"><span data-stu-id="88885-108">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="88885-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="88885-109">EXAMPLES</span></span>

### <span data-ttu-id="88885-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="88885-110">Example 1</span></span>
```
PS C:\> Get-AzIntegrationAccountGeneratedIcn -AgreementType "X12" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "X12IntegrationAccountAgreement"
ControlNumber            : 1000
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="88885-111">To polecenie pobiera numer kontrolki wymiany X12 wygenerowany na koncie integracji według nazwy umowy.</span><span class="sxs-lookup"><span data-stu-id="88885-111">This command gets the integration account generated X12 interchange control number by agreement name.</span></span> <span data-ttu-id="88885-112">Upewnij się, że określona umowa jest typu "X12"</span><span class="sxs-lookup"><span data-stu-id="88885-112">Please make sure agreement specified is of type "X12"</span></span>

### <span data-ttu-id="88885-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="88885-113">Example 2</span></span>
```
PS C:\> Get-AzIntegrationAccountGeneratedIcn -AgreementType "Edifact" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "EdifactIntegrationAccountAgreement"
ControlNumber            : 1000
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="88885-114">To polecenie pobiera numer kontroli wymiany Edifact wygenerowany na koncie integracji według nazwy umowy.</span><span class="sxs-lookup"><span data-stu-id="88885-114">This command gets the integration account generated Edifact interchange control number by agreement name.</span></span> <span data-ttu-id="88885-115">Upewnij się, że określona umowa jest typu "Edifact"</span><span class="sxs-lookup"><span data-stu-id="88885-115">Please make sure agreement specified is of type "Edifact"</span></span>

### <span data-ttu-id="88885-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="88885-116">Example 3</span></span>
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

<span data-ttu-id="88885-117">To polecenie pobiera wszystkie wygenerowane numery kontroli wymiany X12 według nazwy konta integracji.</span><span class="sxs-lookup"><span data-stu-id="88885-117">This command gets all the generated X12 interchange control numbers by integration account name.</span></span>

## <span data-ttu-id="88885-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="88885-118">PARAMETERS</span></span>

### <span data-ttu-id="88885-119">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="88885-119">-AgreementName</span></span>
<span data-ttu-id="88885-120">Nazwa umowy konta integracji.</span><span class="sxs-lookup"><span data-stu-id="88885-120">The integration account agreement name.</span></span>

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

### <span data-ttu-id="88885-121">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="88885-121">-AgreementType</span></span>
<span data-ttu-id="88885-122">Typ umowy konta integracji.</span><span class="sxs-lookup"><span data-stu-id="88885-122">The integration account agreement type.</span></span>

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

### <span data-ttu-id="88885-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88885-123">-DefaultProfile</span></span>
<span data-ttu-id="88885-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="88885-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="88885-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="88885-125">-Name</span></span>
<span data-ttu-id="88885-126">Nazwa konta integracji.</span><span class="sxs-lookup"><span data-stu-id="88885-126">The integration account name.</span></span>

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

### <span data-ttu-id="88885-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88885-127">-ResourceGroupName</span></span>
<span data-ttu-id="88885-128">Nazwa grupy zasobów konta integracji.</span><span class="sxs-lookup"><span data-stu-id="88885-128">The integration account resource group name.</span></span>

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

### <span data-ttu-id="88885-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88885-129">CommonParameters</span></span>
<span data-ttu-id="88885-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88885-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88885-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88885-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88885-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="88885-132">INPUTS</span></span>

### <span data-ttu-id="88885-133">System.String</span><span class="sxs-lookup"><span data-stu-id="88885-133">System.String</span></span>

## <span data-ttu-id="88885-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="88885-134">OUTPUTS</span></span>

### <span data-ttu-id="88885-135">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="88885-135">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="88885-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="88885-136">NOTES</span></span>

## <span data-ttu-id="88885-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="88885-137">RELATED LINKS</span></span>

[<span data-ttu-id="88885-138">Set-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="88885-138">Set-AzIntegrationAccountGeneratedIcn</span></span>](./Set-AzIntegrationAccountGeneratedIcn.md)

