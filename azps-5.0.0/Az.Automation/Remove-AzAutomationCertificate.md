---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: C0B24E18-9163-458A-8297-93CB5C2003FA
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCertificate.md
ms.openlocfilehash: e6dd090998d7a61d61fdad4bb40cbe2c62d7df1f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94307488"
---
# <span data-ttu-id="4b965-101">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="4b965-101">Remove-AzAutomationCertificate</span></span>

## <span data-ttu-id="4b965-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4b965-102">SYNOPSIS</span></span>
<span data-ttu-id="4b965-103">Usuwa certyfikat automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="4b965-103">Removes an Automation certificate.</span></span>

## <span data-ttu-id="4b965-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4b965-104">SYNTAX</span></span>

```
Remove-AzAutomationCertificate [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b965-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4b965-105">DESCRIPTION</span></span>
<span data-ttu-id="4b965-106">Polecenie cmdlet **Remove-AzAutomationCertificate** usuwa certyfikat z usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="4b965-106">The **Remove-AzAutomationCertificate** cmdlet removes a certificate from Azure Automation.</span></span>

## <span data-ttu-id="4b965-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4b965-107">EXAMPLES</span></span>

### <span data-ttu-id="4b965-108">Przykład 1. Usuń certyfikat</span><span class="sxs-lookup"><span data-stu-id="4b965-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzAutomationCertificate -AutomationAccountName "Contoso17" -Name "Cert01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="4b965-109">To polecenie usuwa certyfikat o nazwie Cert01 na koncie automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="4b965-109">This command removes a certificate named Cert01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="4b965-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4b965-110">PARAMETERS</span></span>

### <span data-ttu-id="4b965-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4b965-111">-AutomationAccountName</span></span>
<span data-ttu-id="4b965-112">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet usuwa certyfikat.</span><span class="sxs-lookup"><span data-stu-id="4b965-112">Specifies the name of the Automation account for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="4b965-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b965-113">-DefaultProfile</span></span>
<span data-ttu-id="4b965-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="4b965-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4b965-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4b965-115">-Name</span></span>
<span data-ttu-id="4b965-116">Określa nazwę certyfikatu usuniętego przez ten aplet polecenia.</span><span class="sxs-lookup"><span data-stu-id="4b965-116">Specifies the name of the certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4b965-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b965-117">-ResourceGroupName</span></span>
<span data-ttu-id="4b965-118">Określa nazwę grupy zasobów, dla której ten aplet polecenia usunie certyfikat.</span><span class="sxs-lookup"><span data-stu-id="4b965-118">Specifies the name of the resource group for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="4b965-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4b965-119">-Confirm</span></span>
<span data-ttu-id="4b965-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b965-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b965-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b965-121">-WhatIf</span></span>
<span data-ttu-id="4b965-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b965-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b965-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4b965-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b965-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b965-124">CommonParameters</span></span>
<span data-ttu-id="4b965-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b965-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b965-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b965-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b965-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4b965-127">INPUTS</span></span>

### <span data-ttu-id="4b965-128">System. String</span><span class="sxs-lookup"><span data-stu-id="4b965-128">System.String</span></span>

## <span data-ttu-id="4b965-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4b965-129">OUTPUTS</span></span>

### <span data-ttu-id="4b965-130">System. void</span><span class="sxs-lookup"><span data-stu-id="4b965-130">System.Void</span></span>

## <span data-ttu-id="4b965-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4b965-131">NOTES</span></span>

## <span data-ttu-id="4b965-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4b965-132">RELATED LINKS</span></span>

[<span data-ttu-id="4b965-133">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="4b965-133">Get-AzAutomationCertificate</span></span>](./Get-AzAutomationCertificate.md)

[<span data-ttu-id="4b965-134">Nowe — AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="4b965-134">New-AzAutomationCertificate</span></span>](./New-AzAutomationCertificate.md)

[<span data-ttu-id="4b965-135">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="4b965-135">Set-AzAutomationCertificate</span></span>](./Set-AzAutomationCertificate.md)


