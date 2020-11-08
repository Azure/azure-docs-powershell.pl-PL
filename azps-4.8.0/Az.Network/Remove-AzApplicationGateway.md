---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E9390015-FD5C-4015-BA81-3445ADF8F8BF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGateway.md
ms.openlocfilehash: aa8c40d7fb9f5ccb99ccdd88d6c04ceb4a888bf2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223316"
---
# <span data-ttu-id="da982-101">Remove-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="da982-101">Remove-AzApplicationGateway</span></span>

## <span data-ttu-id="da982-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="da982-102">SYNOPSIS</span></span>
<span data-ttu-id="da982-103">Usuwa bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="da982-103">Removes an application gateway.</span></span>

## <span data-ttu-id="da982-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="da982-104">SYNTAX</span></span>

```
Remove-AzApplicationGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da982-105">Opis</span><span class="sxs-lookup"><span data-stu-id="da982-105">DESCRIPTION</span></span>
<span data-ttu-id="da982-106">Polecenie cmdlet **Remove-AzApplicationGateway** usuwa bramę Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="da982-106">The **Remove-AzApplicationGateway** cmdlet removes an application gateway.</span></span>

## <span data-ttu-id="da982-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="da982-107">EXAMPLES</span></span>

### <span data-ttu-id="da982-108">Przykład 1: usuwanie określonej bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="da982-108">Example 1: Remove a specified application gateway</span></span>
```
PS C:\>Remove-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="da982-109">To polecenie usuwa bramkę Application Gateway o nazwie ApplicationGateway01 w grupie zasobów o nazwie ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="da982-109">This command removes the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="da982-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="da982-110">PARAMETERS</span></span>

### <span data-ttu-id="da982-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da982-111">-DefaultProfile</span></span>
<span data-ttu-id="da982-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="da982-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da982-113">-Force</span><span class="sxs-lookup"><span data-stu-id="da982-113">-Force</span></span>
<span data-ttu-id="da982-114">Wskazuje, że polecenie cmdlet wymusza usunięcie bramy aplikacji bez względu na to, czy są do niego przydzielone zasoby.</span><span class="sxs-lookup"><span data-stu-id="da982-114">Indicates that the cmdlet forces the deletion of the application gateway regardless of whether resources are assigned to it.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da982-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="da982-115">-Name</span></span>
<span data-ttu-id="da982-116">Określa nazwę bramy aplikacji, która ma zostać usunięta.</span><span class="sxs-lookup"><span data-stu-id="da982-116">Specifies the name of the application gateway to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da982-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="da982-117">-PassThru</span></span>
<span data-ttu-id="da982-118">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="da982-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="da982-119">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="da982-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da982-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da982-120">-ResourceGroupName</span></span>
<span data-ttu-id="da982-121">Określa nazwę grupy zasobów, do której należy Brama aplikacji.</span><span class="sxs-lookup"><span data-stu-id="da982-121">Specifies the name of the resource group name that the application gateway belongs to.</span></span>

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

### <span data-ttu-id="da982-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="da982-122">-Confirm</span></span>
<span data-ttu-id="da982-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da982-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da982-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da982-124">-WhatIf</span></span>
<span data-ttu-id="da982-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da982-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da982-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="da982-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da982-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da982-127">CommonParameters</span></span>
<span data-ttu-id="da982-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da982-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da982-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da982-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da982-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="da982-130">INPUTS</span></span>

### <span data-ttu-id="da982-131">System. String</span><span class="sxs-lookup"><span data-stu-id="da982-131">System.String</span></span>

### <span data-ttu-id="da982-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="da982-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="da982-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="da982-133">OUTPUTS</span></span>

### <span data-ttu-id="da982-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="da982-134">System.Boolean</span></span>

## <span data-ttu-id="da982-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="da982-135">NOTES</span></span>

## <span data-ttu-id="da982-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="da982-136">RELATED LINKS</span></span>

[<span data-ttu-id="da982-137">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="da982-137">Set-AzApplicationGateway</span></span>](./Set-AzApplicationGateway.md)


