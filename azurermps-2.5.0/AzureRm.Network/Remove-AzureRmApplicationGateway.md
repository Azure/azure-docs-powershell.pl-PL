---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E9390015-FD5C-4015-BA81-3445ADF8F8BF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgateway
schema: 2.0.0
ms.openlocfilehash: 99ac8e367c42cd59b3f055aa4a86a3efd4f297a0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898278"
---
# <span data-ttu-id="6282e-101">Remove-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6282e-101">Remove-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="6282e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6282e-102">SYNOPSIS</span></span>
<span data-ttu-id="6282e-103">Usuwa bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="6282e-103">Removes an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6282e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6282e-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6282e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6282e-105">DESCRIPTION</span></span>
<span data-ttu-id="6282e-106">Polecenie cmdlet **Remove-AzureRmApplicationGateway** usuwa bramę Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="6282e-106">The **Remove-AzureRmApplicationGateway** cmdlet removes an application gateway.</span></span>

## <span data-ttu-id="6282e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6282e-107">EXAMPLES</span></span>

### <span data-ttu-id="6282e-108">Przykład 1: usuwanie określonej bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="6282e-108">Example 1: Remove a specified application gateway</span></span>
```
PS C:\>Remove-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="6282e-109">To polecenie usuwa bramkę Application Gateway o nazwie ApplicationGateway01 w grupie zasobów o nazwie ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="6282e-109">This command removes the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="6282e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6282e-110">PARAMETERS</span></span>

### <span data-ttu-id="6282e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6282e-111">-DefaultProfile</span></span>
<span data-ttu-id="6282e-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6282e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6282e-113">-Force</span><span class="sxs-lookup"><span data-stu-id="6282e-113">-Force</span></span>
<span data-ttu-id="6282e-114">Wskazuje, że polecenie cmdlet wymusza usunięcie bramy aplikacji bez względu na to, czy są do niego przydzielone zasoby.</span><span class="sxs-lookup"><span data-stu-id="6282e-114">Indicates that the cmdlet forces the deletion of the application gateway regardless of whether resources are assigned to it.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6282e-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6282e-115">-Name</span></span>
<span data-ttu-id="6282e-116">Określa nazwę bramy aplikacji, która ma zostać usunięta.</span><span class="sxs-lookup"><span data-stu-id="6282e-116">Specifies the name of the application gateway to be removed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6282e-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6282e-117">-PassThru</span></span>
<span data-ttu-id="6282e-118">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="6282e-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6282e-119">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="6282e-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6282e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6282e-120">-ResourceGroupName</span></span>
<span data-ttu-id="6282e-121">Określa nazwę grupy zasobów, do której należy Brama aplikacji.</span><span class="sxs-lookup"><span data-stu-id="6282e-121">Specifies the name of the resource group name that the application gateway belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6282e-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6282e-122">-Confirm</span></span>
<span data-ttu-id="6282e-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6282e-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6282e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6282e-124">-WhatIf</span></span>
<span data-ttu-id="6282e-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6282e-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6282e-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6282e-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6282e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6282e-127">CommonParameters</span></span>
<span data-ttu-id="6282e-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6282e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6282e-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6282e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6282e-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6282e-130">INPUTS</span></span>

## <span data-ttu-id="6282e-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6282e-131">OUTPUTS</span></span>

### <span data-ttu-id="6282e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="6282e-132">System.String</span></span>

## <span data-ttu-id="6282e-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6282e-133">NOTES</span></span>

## <span data-ttu-id="6282e-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6282e-134">RELATED LINKS</span></span>

[<span data-ttu-id="6282e-135">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6282e-135">Set-AzureRmApplicationGateway</span></span>](./Set-AzureRmApplicationGateway.md)


