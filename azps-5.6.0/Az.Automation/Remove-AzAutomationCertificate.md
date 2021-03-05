---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: C0B24E18-9163-458A-8297-93CB5C2003FA
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCertificate.md
ms.openlocfilehash: 17eb5530511ccc4303fdb2c978006223e6bd7ed5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009985"
---
# <span data-ttu-id="e0aa6-101">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="e0aa6-101">Remove-AzAutomationCertificate</span></span>

## <span data-ttu-id="e0aa6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0aa6-102">SYNOPSIS</span></span>
<span data-ttu-id="e0aa6-103">Usuwa certyfikat automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="e0aa6-103">Removes an Automation certificate.</span></span>

## <span data-ttu-id="e0aa6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e0aa6-104">SYNTAX</span></span>

```
Remove-AzAutomationCertificate [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0aa6-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e0aa6-105">DESCRIPTION</span></span>
<span data-ttu-id="e0aa6-106">Polecenie **cmdlet Remove-AzAutomationCertificate** usuwa certyfikat z usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="e0aa6-106">The **Remove-AzAutomationCertificate** cmdlet removes a certificate from Azure Automation.</span></span>

## <span data-ttu-id="e0aa6-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e0aa6-107">EXAMPLES</span></span>

### <span data-ttu-id="e0aa6-108">Przykład 1. Usuwanie certyfikatu</span><span class="sxs-lookup"><span data-stu-id="e0aa6-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzAutomationCertificate -AutomationAccountName "Contoso17" -Name "Cert01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="e0aa6-109">To polecenie usuwa certyfikat o nazwie Cert01 z konta automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="e0aa6-109">This command removes a certificate named Cert01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="e0aa6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0aa6-110">PARAMETERS</span></span>

### <span data-ttu-id="e0aa6-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e0aa6-111">-AutomationAccountName</span></span>
<span data-ttu-id="e0aa6-112">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet usuwa certyfikat.</span><span class="sxs-lookup"><span data-stu-id="e0aa6-112">Specifies the name of the Automation account for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="e0aa6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0aa6-113">-DefaultProfile</span></span>
<span data-ttu-id="e0aa6-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="e0aa6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e0aa6-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e0aa6-115">-Name</span></span>
<span data-ttu-id="e0aa6-116">Określa nazwę certyfikatu, który zostanie usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0aa6-116">Specifies the name of the certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e0aa6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0aa6-117">-ResourceGroupName</span></span>
<span data-ttu-id="e0aa6-118">Określa nazwę grupy zasobów, dla której to polecenie cmdlet usuwa certyfikat.</span><span class="sxs-lookup"><span data-stu-id="e0aa6-118">Specifies the name of the resource group for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="e0aa6-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e0aa6-119">-Confirm</span></span>
<span data-ttu-id="e0aa6-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e0aa6-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0aa6-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0aa6-121">-WhatIf</span></span>
<span data-ttu-id="e0aa6-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0aa6-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0aa6-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e0aa6-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0aa6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0aa6-124">CommonParameters</span></span>
<span data-ttu-id="e0aa6-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0aa6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0aa6-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0aa6-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0aa6-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e0aa6-127">INPUTS</span></span>

### <span data-ttu-id="e0aa6-128">System.String</span><span class="sxs-lookup"><span data-stu-id="e0aa6-128">System.String</span></span>

## <span data-ttu-id="e0aa6-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e0aa6-129">OUTPUTS</span></span>

### <span data-ttu-id="e0aa6-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="e0aa6-130">System.Void</span></span>

## <span data-ttu-id="e0aa6-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e0aa6-131">NOTES</span></span>

## <span data-ttu-id="e0aa6-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e0aa6-132">RELATED LINKS</span></span>

[<span data-ttu-id="e0aa6-133">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="e0aa6-133">Get-AzAutomationCertificate</span></span>](./Get-AzAutomationCertificate.md)

[<span data-ttu-id="e0aa6-134">New-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="e0aa6-134">New-AzAutomationCertificate</span></span>](./New-AzAutomationCertificate.md)

[<span data-ttu-id="e0aa6-135">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="e0aa6-135">Set-AzAutomationCertificate</span></span>](./Set-AzAutomationCertificate.md)


