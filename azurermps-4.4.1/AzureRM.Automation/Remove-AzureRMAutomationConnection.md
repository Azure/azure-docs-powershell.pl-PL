---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: C1C0F69D-6A3F-4523-BB70-27676A3DDCBD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationConnection.md
ms.openlocfilehash: aade8dec765a7336292e0350d098417e29d0e360
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548395"
---
# <span data-ttu-id="53386-101">Remove-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="53386-101">Remove-AzureRmAutomationConnection</span></span>

## <span data-ttu-id="53386-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="53386-102">SYNOPSIS</span></span>
<span data-ttu-id="53386-103">Umożliwia usunięcie połączenia automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="53386-103">Removes an Automation connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53386-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="53386-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationConnection [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="53386-105">Opis</span><span class="sxs-lookup"><span data-stu-id="53386-105">DESCRIPTION</span></span>
<span data-ttu-id="53386-106">Polecenie cmdlet **Remove-AzureRmAutomationConnection** usuwa połączenie z usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="53386-106">The **Remove-AzureRmAutomationConnection** cmdlet removes a connection from Azure Automation.</span></span>

## <span data-ttu-id="53386-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="53386-107">EXAMPLES</span></span>

### <span data-ttu-id="53386-108">Przykład 1: Usuwanie połączenia</span><span class="sxs-lookup"><span data-stu-id="53386-108">Example 1: Remove a connection</span></span>
```
PS C:\>Remove-AzureRmAutomationConnection -AutomationAccountName "Contoso17" -Name "ContosoConnection" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="53386-109">To polecenie usuwa certyfikat o nazwie ContosoConnection na koncie automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="53386-109">This command removes a certificate named ContosoConnection in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="53386-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="53386-110">PARAMETERS</span></span>

### <span data-ttu-id="53386-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="53386-111">-AutomationAccountName</span></span>
<span data-ttu-id="53386-112">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet usuwa połączenie.</span><span class="sxs-lookup"><span data-stu-id="53386-112">Specifies the name of the automation account for which this cmdlet removes a connection.</span></span>

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

### <span data-ttu-id="53386-113">-Force</span><span class="sxs-lookup"><span data-stu-id="53386-113">-Force</span></span>
<span data-ttu-id="53386-114">ps_force</span><span class="sxs-lookup"><span data-stu-id="53386-114">ps_force</span></span>

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

### <span data-ttu-id="53386-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="53386-115">-Name</span></span>
<span data-ttu-id="53386-116">Określa nazwę połączenia, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53386-116">Specifies the name of the connection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="53386-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53386-117">-ResourceGroupName</span></span>
<span data-ttu-id="53386-118">Określa nazwę grupy zasobów, dla której to polecenie cmdlet usuwa połączenie.</span><span class="sxs-lookup"><span data-stu-id="53386-118">Specifies the name of the resource group for which this cmdlet removes a connection.</span></span>

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

### <span data-ttu-id="53386-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="53386-119">-Confirm</span></span>
<span data-ttu-id="53386-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53386-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53386-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53386-121">-WhatIf</span></span>
<span data-ttu-id="53386-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53386-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53386-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="53386-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53386-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53386-124">-DefaultProfile</span></span>
<span data-ttu-id="53386-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="53386-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53386-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53386-126">CommonParameters</span></span>
<span data-ttu-id="53386-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53386-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53386-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53386-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53386-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="53386-129">INPUTS</span></span>

## <span data-ttu-id="53386-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="53386-130">OUTPUTS</span></span>

## <span data-ttu-id="53386-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="53386-131">NOTES</span></span>

## <span data-ttu-id="53386-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="53386-132">RELATED LINKS</span></span>

[<span data-ttu-id="53386-133">Get-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="53386-133">Get-AzureRmAutomationConnection</span></span>](./Get-AzureRMAutomationConnection.md)

[<span data-ttu-id="53386-134">Nowe — AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="53386-134">New-AzureRmAutomationConnection</span></span>](./New-AzureRMAutomationConnection.md)

