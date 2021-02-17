---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: C1C0F69D-6A3F-4523-BB70-27676A3DDCBD
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnection.md
ms.openlocfilehash: 1beda1b4db41c2aa3bf40bba7b72e0e684ba3196
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239587"
---
# <span data-ttu-id="b02c3-101">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="b02c3-101">Remove-AzAutomationConnection</span></span>

## <span data-ttu-id="b02c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b02c3-102">SYNOPSIS</span></span>
<span data-ttu-id="b02c3-103">Usuwa połączenie automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="b02c3-103">Removes an Automation connection.</span></span>

## <span data-ttu-id="b02c3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b02c3-104">SYNTAX</span></span>

```
Remove-AzAutomationConnection [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b02c3-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b02c3-105">DESCRIPTION</span></span>
<span data-ttu-id="b02c3-106">Polecenie **cmdlet Remove-AzAutomationConnection** usuwa połączenie z usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="b02c3-106">The **Remove-AzAutomationConnection** cmdlet removes a connection from Azure Automation.</span></span>

## <span data-ttu-id="b02c3-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b02c3-107">EXAMPLES</span></span>

### <span data-ttu-id="b02c3-108">Przykład 1. Usuwanie połączenia</span><span class="sxs-lookup"><span data-stu-id="b02c3-108">Example 1: Remove a connection</span></span>
```
PS C:\>Remove-AzAutomationConnection -AutomationAccountName "Contoso17" -Name "ContosoConnection" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="b02c3-109">To polecenie usuwa certyfikat o nazwie ContosoConnection z konta automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="b02c3-109">This command removes a certificate named ContosoConnection in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="b02c3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b02c3-110">PARAMETERS</span></span>

### <span data-ttu-id="b02c3-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b02c3-111">-AutomationAccountName</span></span>
<span data-ttu-id="b02c3-112">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet usuwa połączenie.</span><span class="sxs-lookup"><span data-stu-id="b02c3-112">Specifies the name of the automation account for which this cmdlet removes a connection.</span></span>

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

### <span data-ttu-id="b02c3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b02c3-113">-DefaultProfile</span></span>
<span data-ttu-id="b02c3-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="b02c3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b02c3-115">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="b02c3-115">-Force</span></span>
<span data-ttu-id="b02c3-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="b02c3-116">ps_force</span></span>

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

### <span data-ttu-id="b02c3-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b02c3-117">-Name</span></span>
<span data-ttu-id="b02c3-118">Określa nazwę połączenia, które usuwa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b02c3-118">Specifies the name of the connection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b02c3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b02c3-119">-ResourceGroupName</span></span>
<span data-ttu-id="b02c3-120">Określa nazwę grupy zasobów, dla której to polecenie cmdlet usuwa połączenie.</span><span class="sxs-lookup"><span data-stu-id="b02c3-120">Specifies the name of the resource group for which this cmdlet removes a connection.</span></span>

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

### <span data-ttu-id="b02c3-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b02c3-121">-Confirm</span></span>
<span data-ttu-id="b02c3-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b02c3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b02c3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b02c3-123">-WhatIf</span></span>
<span data-ttu-id="b02c3-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b02c3-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b02c3-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b02c3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b02c3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b02c3-126">CommonParameters</span></span>
<span data-ttu-id="b02c3-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b02c3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b02c3-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b02c3-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b02c3-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b02c3-129">INPUTS</span></span>

### <span data-ttu-id="b02c3-130">System.String</span><span class="sxs-lookup"><span data-stu-id="b02c3-130">System.String</span></span>

## <span data-ttu-id="b02c3-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b02c3-131">OUTPUTS</span></span>

### <span data-ttu-id="b02c3-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="b02c3-132">System.Void</span></span>

## <span data-ttu-id="b02c3-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b02c3-133">NOTES</span></span>

## <span data-ttu-id="b02c3-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b02c3-134">RELATED LINKS</span></span>

[<span data-ttu-id="b02c3-135">Get-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="b02c3-135">Get-AzAutomationConnection</span></span>](./Get-AzAutomationConnection.md)

[<span data-ttu-id="b02c3-136">New-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="b02c3-136">New-AzAutomationConnection</span></span>](./New-AzAutomationConnection.md)


