---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountReceivedIcn.md
ms.openlocfilehash: be42bd7d3e4a6a839182ae36d71f73377460eceb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527494"
---
# <span data-ttu-id="1467a-101">Get-AzureRmIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="1467a-101">Get-AzureRmIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="1467a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1467a-102">SYNOPSIS</span></span>
<span data-ttu-id="1467a-103">To polecenie cmdlet pobiera określony numer kontrolki wymiany w ramach umowy i wartość numeru sterującego.</span><span class="sxs-lookup"><span data-stu-id="1467a-103">This cmdlet retrieves a specific received interchange control number per agreement and control number value.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1467a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1467a-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1467a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1467a-105">DESCRIPTION</span></span>
<span data-ttu-id="1467a-106">To polecenie cmdlet jest używane w scenariuszach odzyskiwania po awarii w celu sprawdzenia poprawności obecności numeru otrzymanej kontrolki wymiany i opcjonalnie usunięcia tej jednostki za pomocą polecenia Remove-AzureRmIntegrationAccountReceivedIcn.</span><span class="sxs-lookup"><span data-stu-id="1467a-106">This cmdlet is meant to be used in disaster recovery scenarios to validate the presence of a received interchange control number and optionally to remove that entity with Remove-AzureRmIntegrationAccountReceivedIcn.</span></span>
<span data-ttu-id="1467a-107">Podaj parametr "-Agreementtype", aby określić, czy numery kontrolek X12 lub EDIFACT mają być zwracane.</span><span class="sxs-lookup"><span data-stu-id="1467a-107">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="1467a-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1467a-108">EXAMPLES</span></span>

### <span data-ttu-id="1467a-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1467a-109">Example 1</span></span>
```
PS C:\> Get-AzureRmIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="1467a-110">To polecenie uzyskuje konto integracji usługi X12 otrzymało numer kontrolki wymiany według nazwy kontraktu i wartości numeru kontrolnego.</span><span class="sxs-lookup"><span data-stu-id="1467a-110">This command gets the X12 integration account received interchange control number by agreement name and control number value.</span></span>

### <span data-ttu-id="1467a-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="1467a-111">Example 2</span></span>
```
PS C:\> Get-AzureRmIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="1467a-112">To polecenie uzyskuje konto integracji usługi EDIFACT otrzymało numer kontrolki wymiany według nazwy kontraktu i wartości numeru kontrolnego.</span><span class="sxs-lookup"><span data-stu-id="1467a-112">This command gets the Edifact integration account received interchange control number by agreement name and control number value.</span></span>

## <span data-ttu-id="1467a-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1467a-113">PARAMETERS</span></span>

### <span data-ttu-id="1467a-114">-Agreementname</span><span class="sxs-lookup"><span data-stu-id="1467a-114">-AgreementName</span></span>
<span data-ttu-id="1467a-115">Nazwa umowy dotyczącej konta integracji.</span><span class="sxs-lookup"><span data-stu-id="1467a-115">The integration account agreement name.</span></span>

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

### <span data-ttu-id="1467a-116">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="1467a-116">-ControlNumberValue</span></span>
<span data-ttu-id="1467a-117">Wartość numeru kontrolnego konta integracji.</span><span class="sxs-lookup"><span data-stu-id="1467a-117">The integration account control number value.</span></span>

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

### <span data-ttu-id="1467a-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1467a-118">-Name</span></span>
<span data-ttu-id="1467a-119">Nazwa konta integracji.</span><span class="sxs-lookup"><span data-stu-id="1467a-119">The integration account name.</span></span>

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

### <span data-ttu-id="1467a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1467a-120">-ResourceGroupName</span></span>
<span data-ttu-id="1467a-121">Nazwa grupy zasobów konta integracji.</span><span class="sxs-lookup"><span data-stu-id="1467a-121">The integration account resource group name.</span></span>

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

### <span data-ttu-id="1467a-122">-Agreementtype</span><span class="sxs-lookup"><span data-stu-id="1467a-122">-AgreementType</span></span>
<span data-ttu-id="1467a-123">Typ umowy dotyczącej konta integracji.</span><span class="sxs-lookup"><span data-stu-id="1467a-123">The integration account agreement type.</span></span>

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

### <span data-ttu-id="1467a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1467a-124">-DefaultProfile</span></span>
<span data-ttu-id="1467a-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1467a-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1467a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1467a-126">CommonParameters</span></span>
<span data-ttu-id="1467a-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1467a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1467a-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1467a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1467a-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1467a-129">INPUTS</span></span>

### <span data-ttu-id="1467a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="1467a-130">System.String</span></span>

## <span data-ttu-id="1467a-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1467a-131">OUTPUTS</span></span>

### <span data-ttu-id="1467a-132">Microsoft. Azure. Commands. LogicApp. Utilities. IntegrationAccountClient + IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="1467a-132">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountClient+IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="1467a-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1467a-133">NOTES</span></span>

## <span data-ttu-id="1467a-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1467a-134">RELATED LINKS</span></span>

[<span data-ttu-id="1467a-135">Set-AzureRmIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="1467a-135">Set-AzureRmIntegrationAccountReceivedIcn</span></span>](./Set-AzureRmIntegrationAccountReceivedIcn.md)

[<span data-ttu-id="1467a-136">Remove-AzureRmIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="1467a-136">Remove-AzureRmIntegrationAccountReceivedIcn</span></span>](./Remove-AzureRmIntegrationAccountReceivedIcn.md)
