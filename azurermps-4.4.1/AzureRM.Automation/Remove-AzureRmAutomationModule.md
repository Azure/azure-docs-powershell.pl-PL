---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 5F45A12C-BB50-4732-BE80-188491DEF8B5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationModule.md
ms.openlocfilehash: 42fc322e9f593ecad6c295952d46274eb2563799
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547087"
---
# <span data-ttu-id="1ce32-101">Remove-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="1ce32-101">Remove-AzureRmAutomationModule</span></span>

## <span data-ttu-id="1ce32-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1ce32-102">SYNOPSIS</span></span>
<span data-ttu-id="1ce32-103">Umożliwia usunięcie modułu z automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="1ce32-103">Removes a module from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ce32-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1ce32-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationModule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1ce32-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1ce32-105">DESCRIPTION</span></span>
<span data-ttu-id="1ce32-106">Polecenie cmdlet **Remove-AzureRmAutomationModule** umożliwia usunięcie modułu z konta usługi Automation w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="1ce32-106">The **Remove-AzureRmAutomationModule** cmdlet removes a module from an Automation account in Azure Automation.</span></span>

## <span data-ttu-id="1ce32-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1ce32-107">EXAMPLES</span></span>

### <span data-ttu-id="1ce32-108">Przykład 1: usuwanie modułu</span><span class="sxs-lookup"><span data-stu-id="1ce32-108">Example 1: Remove a module</span></span>
```
PS C:\>Remove-AzureRmAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="1ce32-109">To polecenie umożliwia usunięcie modułu o nazwie ContosoModule z konta usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="1ce32-109">This command removes a module named ContosoModule from the Automation account named Contoso17.</span></span>

## <span data-ttu-id="1ce32-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1ce32-110">PARAMETERS</span></span>

### <span data-ttu-id="1ce32-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1ce32-111">-AutomationAccountName</span></span>
<span data-ttu-id="1ce32-112">Określa nazwę konta automatyzacji, na podstawie którego ten aplet polecenia usuwa moduł.</span><span class="sxs-lookup"><span data-stu-id="1ce32-112">Specifies the name of the Automation account from which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="1ce32-113">-Force</span><span class="sxs-lookup"><span data-stu-id="1ce32-113">-Force</span></span>
<span data-ttu-id="1ce32-114">ps_force</span><span class="sxs-lookup"><span data-stu-id="1ce32-114">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ce32-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1ce32-115">-Name</span></span>
<span data-ttu-id="1ce32-116">Określa nazwę modułu, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ce32-116">Specifies the name of the module that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1ce32-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ce32-117">-ResourceGroupName</span></span>
<span data-ttu-id="1ce32-118">Określa nazwę grupy zasobów, w której ten aplet polecenia usunie moduł.</span><span class="sxs-lookup"><span data-stu-id="1ce32-118">Specifies the name of a resource group in which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="1ce32-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1ce32-119">-Confirm</span></span>
<span data-ttu-id="1ce32-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ce32-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ce32-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ce32-121">-WhatIf</span></span>
<span data-ttu-id="1ce32-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ce32-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ce32-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1ce32-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ce32-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ce32-124">-DefaultProfile</span></span>
<span data-ttu-id="1ce32-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1ce32-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ce32-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ce32-126">CommonParameters</span></span>
<span data-ttu-id="1ce32-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ce32-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ce32-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ce32-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ce32-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1ce32-129">INPUTS</span></span>

## <span data-ttu-id="1ce32-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1ce32-130">OUTPUTS</span></span>

## <span data-ttu-id="1ce32-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1ce32-131">NOTES</span></span>

## <span data-ttu-id="1ce32-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1ce32-132">RELATED LINKS</span></span>

[<span data-ttu-id="1ce32-133">Get-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="1ce32-133">Get-AzureRmAutomationModule</span></span>](./Get-AzureRmAutomationModule.md)

[<span data-ttu-id="1ce32-134">Nowe — AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="1ce32-134">New-AzureRmAutomationModule</span></span>](./New-AzureRmAutomationModule.md)

[<span data-ttu-id="1ce32-135">Set-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="1ce32-135">Set-AzureRmAutomationModule</span></span>](./Set-AzureRmAutomationModule.md)


