---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: C0B24E18-9163-458A-8297-93CB5C2003FA
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCertificate.md
ms.openlocfilehash: e6dd090998d7a61d61fdad4bb40cbe2c62d7df1f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94064556"
---
# <span data-ttu-id="88f35-101">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="88f35-101">Remove-AzAutomationCertificate</span></span>

## <span data-ttu-id="88f35-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="88f35-102">SYNOPSIS</span></span>
<span data-ttu-id="88f35-103">Usuwa certyfikat automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="88f35-103">Removes an Automation certificate.</span></span>

## <span data-ttu-id="88f35-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="88f35-104">SYNTAX</span></span>

```
Remove-AzAutomationCertificate [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88f35-105">Opis</span><span class="sxs-lookup"><span data-stu-id="88f35-105">DESCRIPTION</span></span>
<span data-ttu-id="88f35-106">Polecenie cmdlet **Remove-AzAutomationCertificate** usuwa certyfikat z usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="88f35-106">The **Remove-AzAutomationCertificate** cmdlet removes a certificate from Azure Automation.</span></span>

## <span data-ttu-id="88f35-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="88f35-107">EXAMPLES</span></span>

### <span data-ttu-id="88f35-108">Przykład 1. Usuń certyfikat</span><span class="sxs-lookup"><span data-stu-id="88f35-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzAutomationCertificate -AutomationAccountName "Contoso17" -Name "Cert01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="88f35-109">To polecenie usuwa certyfikat o nazwie Cert01 na koncie automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="88f35-109">This command removes a certificate named Cert01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="88f35-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="88f35-110">PARAMETERS</span></span>

### <span data-ttu-id="88f35-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="88f35-111">-AutomationAccountName</span></span>
<span data-ttu-id="88f35-112">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet usuwa certyfikat.</span><span class="sxs-lookup"><span data-stu-id="88f35-112">Specifies the name of the Automation account for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="88f35-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88f35-113">-DefaultProfile</span></span>
<span data-ttu-id="88f35-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="88f35-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="88f35-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="88f35-115">-Name</span></span>
<span data-ttu-id="88f35-116">Określa nazwę certyfikatu usuniętego przez ten aplet polecenia.</span><span class="sxs-lookup"><span data-stu-id="88f35-116">Specifies the name of the certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="88f35-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88f35-117">-ResourceGroupName</span></span>
<span data-ttu-id="88f35-118">Określa nazwę grupy zasobów, dla której ten aplet polecenia usunie certyfikat.</span><span class="sxs-lookup"><span data-stu-id="88f35-118">Specifies the name of the resource group for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="88f35-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="88f35-119">-Confirm</span></span>
<span data-ttu-id="88f35-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88f35-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88f35-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88f35-121">-WhatIf</span></span>
<span data-ttu-id="88f35-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88f35-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88f35-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="88f35-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88f35-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88f35-124">CommonParameters</span></span>
<span data-ttu-id="88f35-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88f35-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88f35-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88f35-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88f35-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="88f35-127">INPUTS</span></span>

### <span data-ttu-id="88f35-128">System. String</span><span class="sxs-lookup"><span data-stu-id="88f35-128">System.String</span></span>

## <span data-ttu-id="88f35-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="88f35-129">OUTPUTS</span></span>

### <span data-ttu-id="88f35-130">System. void</span><span class="sxs-lookup"><span data-stu-id="88f35-130">System.Void</span></span>

## <span data-ttu-id="88f35-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="88f35-131">NOTES</span></span>

## <span data-ttu-id="88f35-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="88f35-132">RELATED LINKS</span></span>

[<span data-ttu-id="88f35-133">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="88f35-133">Get-AzAutomationCertificate</span></span>](./Get-AzAutomationCertificate.md)

[<span data-ttu-id="88f35-134">Nowe — AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="88f35-134">New-AzAutomationCertificate</span></span>](./New-AzAutomationCertificate.md)

[<span data-ttu-id="88f35-135">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="88f35-135">Set-AzAutomationCertificate</span></span>](./Set-AzAutomationCertificate.md)


