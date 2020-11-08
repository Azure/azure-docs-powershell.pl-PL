---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountReceivedIcn.md
ms.openlocfilehash: d7c6e5cfc1462e0ae807c9cdddb2d743a7608738
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94234636"
---
# <span data-ttu-id="40c42-101">Get-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="40c42-101">Get-AzIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="40c42-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="40c42-102">SYNOPSIS</span></span>
<span data-ttu-id="40c42-103">To polecenie cmdlet pobiera określony numer kontrolki wymiany w ramach umowy i wartość numeru sterującego.</span><span class="sxs-lookup"><span data-stu-id="40c42-103">This cmdlet retrieves a specific received interchange control number per agreement and control number value.</span></span>

## <span data-ttu-id="40c42-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="40c42-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="40c42-105">Opis</span><span class="sxs-lookup"><span data-stu-id="40c42-105">DESCRIPTION</span></span>
<span data-ttu-id="40c42-106">To polecenie cmdlet jest używane w scenariuszach odzyskiwania po awarii w celu sprawdzenia poprawności obecności numeru otrzymanej kontrolki wymiany i opcjonalnie usunięcia tej jednostki za pomocą polecenia Remove-AzIntegrationAccountReceivedIcn.</span><span class="sxs-lookup"><span data-stu-id="40c42-106">This cmdlet is meant to be used in disaster recovery scenarios to validate the presence of a received interchange control number and optionally to remove that entity with Remove-AzIntegrationAccountReceivedIcn.</span></span>
<span data-ttu-id="40c42-107">Podaj parametr "-Agreementtype", aby określić, czy numery kontrolek X12 lub EDIFACT mają być zwracane.</span><span class="sxs-lookup"><span data-stu-id="40c42-107">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="40c42-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="40c42-108">EXAMPLES</span></span>

### <span data-ttu-id="40c42-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="40c42-109">Example 1</span></span>
```
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="40c42-110">To polecenie uzyskuje konto integracji usługi X12 otrzymało numer kontrolki wymiany według nazwy kontraktu i wartości numeru kontrolnego.</span><span class="sxs-lookup"><span data-stu-id="40c42-110">This command gets the X12 integration account received interchange control number by agreement name and control number value.</span></span>

### <span data-ttu-id="40c42-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="40c42-111">Example 2</span></span>
```
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="40c42-112">To polecenie uzyskuje konto integracji usługi EDIFACT otrzymało numer kontrolki wymiany według nazwy kontraktu i wartości numeru kontrolnego.</span><span class="sxs-lookup"><span data-stu-id="40c42-112">This command gets the Edifact integration account received interchange control number by agreement name and control number value.</span></span>

## <span data-ttu-id="40c42-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="40c42-113">PARAMETERS</span></span>

### <span data-ttu-id="40c42-114">-Agreementname</span><span class="sxs-lookup"><span data-stu-id="40c42-114">-AgreementName</span></span>
<span data-ttu-id="40c42-115">Nazwa umowy dotyczącej konta integracji.</span><span class="sxs-lookup"><span data-stu-id="40c42-115">The integration account agreement name.</span></span>

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

### <span data-ttu-id="40c42-116">-Agreementtype</span><span class="sxs-lookup"><span data-stu-id="40c42-116">-AgreementType</span></span>
<span data-ttu-id="40c42-117">Typ umowy dotyczącej konta integracji.</span><span class="sxs-lookup"><span data-stu-id="40c42-117">The integration account agreement type.</span></span>

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

### <span data-ttu-id="40c42-118">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="40c42-118">-ControlNumberValue</span></span>
<span data-ttu-id="40c42-119">Wartość numeru kontrolnego konta integracji.</span><span class="sxs-lookup"><span data-stu-id="40c42-119">The integration account control number value.</span></span>

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

### <span data-ttu-id="40c42-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40c42-120">-DefaultProfile</span></span>
<span data-ttu-id="40c42-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="40c42-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="40c42-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="40c42-122">-Name</span></span>
<span data-ttu-id="40c42-123">Nazwa konta integracji.</span><span class="sxs-lookup"><span data-stu-id="40c42-123">The integration account name.</span></span>

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

### <span data-ttu-id="40c42-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40c42-124">-ResourceGroupName</span></span>
<span data-ttu-id="40c42-125">Nazwa grupy zasobów konta integracji.</span><span class="sxs-lookup"><span data-stu-id="40c42-125">The integration account resource group name.</span></span>

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

### <span data-ttu-id="40c42-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40c42-126">CommonParameters</span></span>
<span data-ttu-id="40c42-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40c42-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40c42-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40c42-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40c42-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="40c42-129">INPUTS</span></span>

### <span data-ttu-id="40c42-130">System. String</span><span class="sxs-lookup"><span data-stu-id="40c42-130">System.String</span></span>

## <span data-ttu-id="40c42-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="40c42-131">OUTPUTS</span></span>

### <span data-ttu-id="40c42-132">Microsoft. Azure. Commands. LogicApp. Utilities. IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="40c42-132">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="40c42-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="40c42-133">NOTES</span></span>

## <span data-ttu-id="40c42-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="40c42-134">RELATED LINKS</span></span>

[<span data-ttu-id="40c42-135">Set-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="40c42-135">Set-AzIntegrationAccountReceivedIcn</span></span>](./Set-AzIntegrationAccountReceivedIcn.md)

[<span data-ttu-id="40c42-136">Remove-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="40c42-136">Remove-AzIntegrationAccountReceivedIcn</span></span>](./Remove-AzIntegrationAccountReceivedIcn.md)
