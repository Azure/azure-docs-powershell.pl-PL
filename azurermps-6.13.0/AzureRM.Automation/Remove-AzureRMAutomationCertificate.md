---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: C0B24E18-9163-458A-8297-93CB5C2003FA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCertificate.md
ms.openlocfilehash: 7498310c232fd623b131bdf9ae59136d9a4c500a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547632"
---
# <span data-ttu-id="68aa8-101">Remove-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="68aa8-101">Remove-AzureRmAutomationCertificate</span></span>

## <span data-ttu-id="68aa8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="68aa8-102">SYNOPSIS</span></span>
<span data-ttu-id="68aa8-103">Usuwa certyfikat automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="68aa8-103">Removes an Automation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68aa8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="68aa8-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationCertificate [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="68aa8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="68aa8-105">DESCRIPTION</span></span>
<span data-ttu-id="68aa8-106">Polecenie cmdlet **Remove-AzureRmAutomationCertificate** usuwa certyfikat z usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="68aa8-106">The **Remove-AzureRmAutomationCertificate** cmdlet removes a certificate from Azure Automation.</span></span>

## <span data-ttu-id="68aa8-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="68aa8-107">EXAMPLES</span></span>

### <span data-ttu-id="68aa8-108">Przykład 1. Usuń certyfikat</span><span class="sxs-lookup"><span data-stu-id="68aa8-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzureRmAutomationCertificate -AutomationAccountName "Contoso17" -Name "Cert01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="68aa8-109">To polecenie usuwa certyfikat o nazwie Cert01 na koncie automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="68aa8-109">This command removes a certificate named Cert01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="68aa8-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="68aa8-110">PARAMETERS</span></span>

### <span data-ttu-id="68aa8-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="68aa8-111">-AutomationAccountName</span></span>
<span data-ttu-id="68aa8-112">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet usuwa certyfikat.</span><span class="sxs-lookup"><span data-stu-id="68aa8-112">Specifies the name of the Automation account for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="68aa8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68aa8-113">-DefaultProfile</span></span>
<span data-ttu-id="68aa8-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="68aa8-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="68aa8-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="68aa8-115">-Name</span></span>
<span data-ttu-id="68aa8-116">Określa nazwę certyfikatu usuniętego przez ten aplet polecenia.</span><span class="sxs-lookup"><span data-stu-id="68aa8-116">Specifies the name of the certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="68aa8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68aa8-117">-ResourceGroupName</span></span>
<span data-ttu-id="68aa8-118">Określa nazwę grupy zasobów, dla której ten aplet polecenia usunie certyfikat.</span><span class="sxs-lookup"><span data-stu-id="68aa8-118">Specifies the name of the resource group for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="68aa8-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="68aa8-119">-Confirm</span></span>
<span data-ttu-id="68aa8-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68aa8-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68aa8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68aa8-121">-WhatIf</span></span>
<span data-ttu-id="68aa8-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68aa8-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68aa8-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="68aa8-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68aa8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68aa8-124">CommonParameters</span></span>
<span data-ttu-id="68aa8-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68aa8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68aa8-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68aa8-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68aa8-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="68aa8-127">INPUTS</span></span>

### <span data-ttu-id="68aa8-128">System. String</span><span class="sxs-lookup"><span data-stu-id="68aa8-128">System.String</span></span>

## <span data-ttu-id="68aa8-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="68aa8-129">OUTPUTS</span></span>

### <span data-ttu-id="68aa8-130">System. void</span><span class="sxs-lookup"><span data-stu-id="68aa8-130">System.Void</span></span>

## <span data-ttu-id="68aa8-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="68aa8-131">NOTES</span></span>

## <span data-ttu-id="68aa8-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="68aa8-132">RELATED LINKS</span></span>

[<span data-ttu-id="68aa8-133">Get-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="68aa8-133">Get-AzureRmAutomationCertificate</span></span>](./Get-AzureRMAutomationCertificate.md)

[<span data-ttu-id="68aa8-134">Nowe — AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="68aa8-134">New-AzureRmAutomationCertificate</span></span>](./New-AzureRMAutomationCertificate.md)

[<span data-ttu-id="68aa8-135">Set-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="68aa8-135">Set-AzureRmAutomationCertificate</span></span>](./Set-AzureRMAutomationCertificate.md)


