---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: C0B24E18-9163-458A-8297-93CB5C2003FA
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCertificate.md
ms.openlocfilehash: 9932627e94a27c1b29d20a5a6bc49d47a55d3ef5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706742"
---
# <span data-ttu-id="f95b0-101">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="f95b0-101">Remove-AzAutomationCertificate</span></span>

## <span data-ttu-id="f95b0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f95b0-102">SYNOPSIS</span></span>
<span data-ttu-id="f95b0-103">Usuwa certyfikat automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="f95b0-103">Removes an Automation certificate.</span></span>

## <span data-ttu-id="f95b0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f95b0-104">SYNTAX</span></span>

```
Remove-AzAutomationCertificate [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f95b0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f95b0-105">DESCRIPTION</span></span>
<span data-ttu-id="f95b0-106">Polecenie cmdlet **Remove-AzAutomationCertificate** usuwa certyfikat z usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="f95b0-106">The **Remove-AzAutomationCertificate** cmdlet removes a certificate from Azure Automation.</span></span>

## <span data-ttu-id="f95b0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f95b0-107">EXAMPLES</span></span>

### <span data-ttu-id="f95b0-108">Przykład 1. Usuń certyfikat</span><span class="sxs-lookup"><span data-stu-id="f95b0-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzAutomationCertificate -AutomationAccountName "Contoso17" -Name "Cert01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f95b0-109">To polecenie usuwa certyfikat o nazwie Cert01 na koncie automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="f95b0-109">This command removes a certificate named Cert01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="f95b0-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f95b0-110">PARAMETERS</span></span>

### <span data-ttu-id="f95b0-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f95b0-111">-AutomationAccountName</span></span>
<span data-ttu-id="f95b0-112">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet usuwa certyfikat.</span><span class="sxs-lookup"><span data-stu-id="f95b0-112">Specifies the name of the Automation account for which this cmdlet removes a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f95b0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f95b0-113">-DefaultProfile</span></span>
<span data-ttu-id="f95b0-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f95b0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f95b0-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f95b0-115">-Name</span></span>
<span data-ttu-id="f95b0-116">Określa nazwę certyfikatu usuniętego przez ten aplet polecenia.</span><span class="sxs-lookup"><span data-stu-id="f95b0-116">Specifies the name of the certificate that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f95b0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f95b0-117">-ResourceGroupName</span></span>
<span data-ttu-id="f95b0-118">Określa nazwę grupy zasobów, dla której ten aplet polecenia usunie certyfikat.</span><span class="sxs-lookup"><span data-stu-id="f95b0-118">Specifies the name of the resource group for which this cmdlet removes a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f95b0-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f95b0-119">-Confirm</span></span>
<span data-ttu-id="f95b0-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f95b0-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f95b0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f95b0-121">-WhatIf</span></span>
<span data-ttu-id="f95b0-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f95b0-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f95b0-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f95b0-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f95b0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f95b0-124">CommonParameters</span></span>
<span data-ttu-id="f95b0-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f95b0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f95b0-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f95b0-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f95b0-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f95b0-127">INPUTS</span></span>

### <span data-ttu-id="f95b0-128">System. String</span><span class="sxs-lookup"><span data-stu-id="f95b0-128">System.String</span></span>

## <span data-ttu-id="f95b0-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f95b0-129">OUTPUTS</span></span>

### <span data-ttu-id="f95b0-130">System. void</span><span class="sxs-lookup"><span data-stu-id="f95b0-130">System.Void</span></span>

## <span data-ttu-id="f95b0-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f95b0-131">NOTES</span></span>

## <span data-ttu-id="f95b0-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f95b0-132">RELATED LINKS</span></span>

[<span data-ttu-id="f95b0-133">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="f95b0-133">Get-AzAutomationCertificate</span></span>](./Get-AzAutomationCertificate.md)

[<span data-ttu-id="f95b0-134">Nowe — AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="f95b0-134">New-AzAutomationCertificate</span></span>](./New-AzAutomationCertificate.md)

[<span data-ttu-id="f95b0-135">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="f95b0-135">Set-AzAutomationCertificate</span></span>](./Set-AzAutomationCertificate.md)

