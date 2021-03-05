---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountReceivedIcn.md
ms.openlocfilehash: df7266548b616615fa45131c21f40622894ffe9e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960577"
---
# <span data-ttu-id="ed3ca-101">Get-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="ed3ca-101">Get-AzIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="ed3ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed3ca-102">SYNOPSIS</span></span>
<span data-ttu-id="ed3ca-103">To polecenie cmdlet pobiera określony otrzymany numer kontroli interchange na umowę i wartość numeru kontrolki.</span><span class="sxs-lookup"><span data-stu-id="ed3ca-103">This cmdlet retrieves a specific received interchange control number per agreement and control number value.</span></span>

## <span data-ttu-id="ed3ca-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ed3ca-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ed3ca-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ed3ca-105">DESCRIPTION</span></span>
<span data-ttu-id="ed3ca-106">To polecenie cmdlet jest przeznaczone do użycia w scenariuszach odzyskiwania po awarii w celu zweryfikowania obecności otrzymanego numeru kontroli wymiany i opcjonalnego usunięcia tej jednostki za pomocą funkcji Remove-AzIntegrationAccountReceivedIcn.</span><span class="sxs-lookup"><span data-stu-id="ed3ca-106">This cmdlet is meant to be used in disaster recovery scenarios to validate the presence of a received interchange control number and optionally to remove that entity with Remove-AzIntegrationAccountReceivedIcn.</span></span>
<span data-ttu-id="ed3ca-107">Podaj parametr "-AgreementType", aby określić, czy mają być zwracane numery kontrolek X12, czy Edifact.</span><span class="sxs-lookup"><span data-stu-id="ed3ca-107">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="ed3ca-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ed3ca-108">EXAMPLES</span></span>

### <span data-ttu-id="ed3ca-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ed3ca-109">Example 1</span></span>
```
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="ed3ca-110">To polecenie pobiera numer kontroli wymiany konta integracji X12 według nazwy umowy i wartości numeru kontrolki.</span><span class="sxs-lookup"><span data-stu-id="ed3ca-110">This command gets the X12 integration account received interchange control number by agreement name and control number value.</span></span>

### <span data-ttu-id="ed3ca-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="ed3ca-111">Example 2</span></span>
```
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="ed3ca-112">To polecenie pobiera numer kontroli wymiany konta integracji Edifact według nazwy umowy i wartości numeru kontrolki.</span><span class="sxs-lookup"><span data-stu-id="ed3ca-112">This command gets the Edifact integration account received interchange control number by agreement name and control number value.</span></span>

## <span data-ttu-id="ed3ca-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ed3ca-113">PARAMETERS</span></span>

### <span data-ttu-id="ed3ca-114">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="ed3ca-114">-AgreementName</span></span>
<span data-ttu-id="ed3ca-115">Nazwa umowy konta integracji.</span><span class="sxs-lookup"><span data-stu-id="ed3ca-115">The integration account agreement name.</span></span>

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

### <span data-ttu-id="ed3ca-116">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="ed3ca-116">-AgreementType</span></span>
<span data-ttu-id="ed3ca-117">Typ umowy konta integracji.</span><span class="sxs-lookup"><span data-stu-id="ed3ca-117">The integration account agreement type.</span></span>

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

### <span data-ttu-id="ed3ca-118">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="ed3ca-118">-ControlNumberValue</span></span>
<span data-ttu-id="ed3ca-119">Wartość numeru kontrolki konta integracji.</span><span class="sxs-lookup"><span data-stu-id="ed3ca-119">The integration account control number value.</span></span>

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

### <span data-ttu-id="ed3ca-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed3ca-120">-DefaultProfile</span></span>
<span data-ttu-id="ed3ca-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="ed3ca-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ed3ca-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ed3ca-122">-Name</span></span>
<span data-ttu-id="ed3ca-123">Nazwa konta integracji.</span><span class="sxs-lookup"><span data-stu-id="ed3ca-123">The integration account name.</span></span>

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

### <span data-ttu-id="ed3ca-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed3ca-124">-ResourceGroupName</span></span>
<span data-ttu-id="ed3ca-125">Nazwa grupy zasobów konta integracji.</span><span class="sxs-lookup"><span data-stu-id="ed3ca-125">The integration account resource group name.</span></span>

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

### <span data-ttu-id="ed3ca-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed3ca-126">CommonParameters</span></span>
<span data-ttu-id="ed3ca-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed3ca-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed3ca-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed3ca-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed3ca-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ed3ca-129">INPUTS</span></span>

### <span data-ttu-id="ed3ca-130">System.String</span><span class="sxs-lookup"><span data-stu-id="ed3ca-130">System.String</span></span>

## <span data-ttu-id="ed3ca-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ed3ca-131">OUTPUTS</span></span>

### <span data-ttu-id="ed3ca-132">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="ed3ca-132">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="ed3ca-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ed3ca-133">NOTES</span></span>

## <span data-ttu-id="ed3ca-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ed3ca-134">RELATED LINKS</span></span>

[<span data-ttu-id="ed3ca-135">Set-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="ed3ca-135">Set-AzIntegrationAccountReceivedIcn</span></span>](./Set-AzIntegrationAccountReceivedIcn.md)

[<span data-ttu-id="ed3ca-136">Remove-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="ed3ca-136">Remove-AzIntegrationAccountReceivedIcn</span></span>](./Remove-AzIntegrationAccountReceivedIcn.md)
