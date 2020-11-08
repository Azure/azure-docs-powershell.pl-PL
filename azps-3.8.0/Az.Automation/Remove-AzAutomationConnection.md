---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: C1C0F69D-6A3F-4523-BB70-27676A3DDCBD
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnection.md
ms.openlocfilehash: 1beda1b4db41c2aa3bf40bba7b72e0e684ba3196
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053902"
---
# <span data-ttu-id="17054-101">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="17054-101">Remove-AzAutomationConnection</span></span>

## <span data-ttu-id="17054-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="17054-102">SYNOPSIS</span></span>
<span data-ttu-id="17054-103">Umożliwia usunięcie połączenia automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="17054-103">Removes an Automation connection.</span></span>

## <span data-ttu-id="17054-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="17054-104">SYNTAX</span></span>

```
Remove-AzAutomationConnection [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="17054-105">Opis</span><span class="sxs-lookup"><span data-stu-id="17054-105">DESCRIPTION</span></span>
<span data-ttu-id="17054-106">Polecenie cmdlet **Remove-AzAutomationConnection** usuwa połączenie z usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="17054-106">The **Remove-AzAutomationConnection** cmdlet removes a connection from Azure Automation.</span></span>

## <span data-ttu-id="17054-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="17054-107">EXAMPLES</span></span>

### <span data-ttu-id="17054-108">Przykład 1: Usuwanie połączenia</span><span class="sxs-lookup"><span data-stu-id="17054-108">Example 1: Remove a connection</span></span>
```
PS C:\>Remove-AzAutomationConnection -AutomationAccountName "Contoso17" -Name "ContosoConnection" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="17054-109">To polecenie usuwa certyfikat o nazwie ContosoConnection na koncie automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="17054-109">This command removes a certificate named ContosoConnection in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="17054-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="17054-110">PARAMETERS</span></span>

### <span data-ttu-id="17054-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="17054-111">-AutomationAccountName</span></span>
<span data-ttu-id="17054-112">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet usuwa połączenie.</span><span class="sxs-lookup"><span data-stu-id="17054-112">Specifies the name of the automation account for which this cmdlet removes a connection.</span></span>

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

### <span data-ttu-id="17054-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17054-113">-DefaultProfile</span></span>
<span data-ttu-id="17054-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="17054-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="17054-115">-Force</span><span class="sxs-lookup"><span data-stu-id="17054-115">-Force</span></span>
<span data-ttu-id="17054-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="17054-116">ps_force</span></span>

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

### <span data-ttu-id="17054-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="17054-117">-Name</span></span>
<span data-ttu-id="17054-118">Określa nazwę połączenia, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17054-118">Specifies the name of the connection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="17054-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17054-119">-ResourceGroupName</span></span>
<span data-ttu-id="17054-120">Określa nazwę grupy zasobów, dla której to polecenie cmdlet usuwa połączenie.</span><span class="sxs-lookup"><span data-stu-id="17054-120">Specifies the name of the resource group for which this cmdlet removes a connection.</span></span>

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

### <span data-ttu-id="17054-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="17054-121">-Confirm</span></span>
<span data-ttu-id="17054-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17054-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17054-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17054-123">-WhatIf</span></span>
<span data-ttu-id="17054-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17054-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17054-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="17054-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17054-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17054-126">CommonParameters</span></span>
<span data-ttu-id="17054-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17054-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17054-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17054-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17054-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="17054-129">INPUTS</span></span>

### <span data-ttu-id="17054-130">System. String</span><span class="sxs-lookup"><span data-stu-id="17054-130">System.String</span></span>

## <span data-ttu-id="17054-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="17054-131">OUTPUTS</span></span>

### <span data-ttu-id="17054-132">System. void</span><span class="sxs-lookup"><span data-stu-id="17054-132">System.Void</span></span>

## <span data-ttu-id="17054-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="17054-133">NOTES</span></span>

## <span data-ttu-id="17054-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="17054-134">RELATED LINKS</span></span>

[<span data-ttu-id="17054-135">Get-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="17054-135">Get-AzAutomationConnection</span></span>](./Get-AzAutomationConnection.md)

[<span data-ttu-id="17054-136">Nowe — AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="17054-136">New-AzAutomationConnection</span></span>](./New-AzAutomationConnection.md)


