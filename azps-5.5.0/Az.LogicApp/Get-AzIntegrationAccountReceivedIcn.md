---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountReceivedIcn.md
ms.openlocfilehash: d7c6e5cfc1462e0ae807c9cdddb2d743a7608738
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187626"
---
# <span data-ttu-id="a7382-101">Get-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="a7382-101">Get-AzIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="a7382-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7382-102">SYNOPSIS</span></span>
<span data-ttu-id="a7382-103">To polecenie cmdlet pobiera określony otrzymany numer kontrolki interchange na umowę i wartość numeru kontrolki.</span><span class="sxs-lookup"><span data-stu-id="a7382-103">This cmdlet retrieves a specific received interchange control number per agreement and control number value.</span></span>

## <span data-ttu-id="a7382-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a7382-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a7382-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a7382-105">DESCRIPTION</span></span>
<span data-ttu-id="a7382-106">To polecenie cmdlet jest przeznaczone do użycia w scenariuszach odzyskiwania po awarii w celu weryfikacji obecności otrzymanego numeru kontroli wymiany i opcjonalnego usunięcia tej jednostki za pomocą funkcji Remove-AzIntegrationAccountReceivedIcn.</span><span class="sxs-lookup"><span data-stu-id="a7382-106">This cmdlet is meant to be used in disaster recovery scenarios to validate the presence of a received interchange control number and optionally to remove that entity with Remove-AzIntegrationAccountReceivedIcn.</span></span>
<span data-ttu-id="a7382-107">Podaj parametr "-AgreementType", aby określić, czy mają być zwracane numery kontrolek X12, czy Edifact.</span><span class="sxs-lookup"><span data-stu-id="a7382-107">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="a7382-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a7382-108">EXAMPLES</span></span>

### <span data-ttu-id="a7382-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a7382-109">Example 1</span></span>
```
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="a7382-110">To polecenie pobiera numer kontroli wymiany konta integracji X12 według nazwy umowy i wartości numeru kontrolki.</span><span class="sxs-lookup"><span data-stu-id="a7382-110">This command gets the X12 integration account received interchange control number by agreement name and control number value.</span></span>

### <span data-ttu-id="a7382-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a7382-111">Example 2</span></span>
```
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="a7382-112">To polecenie pobiera numer kontroli wymiany konta integracji Edifact według nazwy umowy i wartości numeru kontrolki.</span><span class="sxs-lookup"><span data-stu-id="a7382-112">This command gets the Edifact integration account received interchange control number by agreement name and control number value.</span></span>

## <span data-ttu-id="a7382-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a7382-113">PARAMETERS</span></span>

### <span data-ttu-id="a7382-114">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="a7382-114">-AgreementName</span></span>
<span data-ttu-id="a7382-115">Nazwa umowy konta integracji.</span><span class="sxs-lookup"><span data-stu-id="a7382-115">The integration account agreement name.</span></span>

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

### <span data-ttu-id="a7382-116">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="a7382-116">-AgreementType</span></span>
<span data-ttu-id="a7382-117">Typ umowy konta integracji.</span><span class="sxs-lookup"><span data-stu-id="a7382-117">The integration account agreement type.</span></span>

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

### <span data-ttu-id="a7382-118">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="a7382-118">-ControlNumberValue</span></span>
<span data-ttu-id="a7382-119">Wartość numeru kontrolki konta integracji.</span><span class="sxs-lookup"><span data-stu-id="a7382-119">The integration account control number value.</span></span>

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

### <span data-ttu-id="a7382-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7382-120">-DefaultProfile</span></span>
<span data-ttu-id="a7382-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="a7382-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a7382-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a7382-122">-Name</span></span>
<span data-ttu-id="a7382-123">Nazwa konta integracji.</span><span class="sxs-lookup"><span data-stu-id="a7382-123">The integration account name.</span></span>

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

### <span data-ttu-id="a7382-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7382-124">-ResourceGroupName</span></span>
<span data-ttu-id="a7382-125">Nazwa grupy zasobów konta integracji.</span><span class="sxs-lookup"><span data-stu-id="a7382-125">The integration account resource group name.</span></span>

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

### <span data-ttu-id="a7382-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7382-126">CommonParameters</span></span>
<span data-ttu-id="a7382-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7382-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7382-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7382-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7382-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a7382-129">INPUTS</span></span>

### <span data-ttu-id="a7382-130">System.String</span><span class="sxs-lookup"><span data-stu-id="a7382-130">System.String</span></span>

## <span data-ttu-id="a7382-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a7382-131">OUTPUTS</span></span>

### <span data-ttu-id="a7382-132">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="a7382-132">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="a7382-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a7382-133">NOTES</span></span>

## <span data-ttu-id="a7382-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a7382-134">RELATED LINKS</span></span>

[<span data-ttu-id="a7382-135">Set-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="a7382-135">Set-AzIntegrationAccountReceivedIcn</span></span>](./Set-AzIntegrationAccountReceivedIcn.md)

[<span data-ttu-id="a7382-136">Remove-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="a7382-136">Remove-AzIntegrationAccountReceivedIcn</span></span>](./Remove-AzIntegrationAccountReceivedIcn.md)
