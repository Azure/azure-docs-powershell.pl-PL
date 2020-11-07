---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C83A0465-45EF-4FCC-B706-D5DF819664F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkinterface
schema: 2.0.0
ms.openlocfilehash: 955c5200b7c7b9716e096f1157f7179619ae4f5c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897565"
---
# <span data-ttu-id="9ea8d-101">Remove-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="9ea8d-101">Remove-AzureRmNetworkInterface</span></span>

## <span data-ttu-id="9ea8d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9ea8d-102">SYNOPSIS</span></span>
<span data-ttu-id="9ea8d-103">Usuwa interfejs sieciowy.</span><span class="sxs-lookup"><span data-stu-id="9ea8d-103">Removes a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ea8d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9ea8d-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ea8d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9ea8d-105">DESCRIPTION</span></span>
<span data-ttu-id="9ea8d-106">Polecenie cmdlet **Remove-AzureRmNetworkInterface** Usuwa interfejs sieci Azure.</span><span class="sxs-lookup"><span data-stu-id="9ea8d-106">The **Remove-AzureRmNetworkInterface** cmdlet removes an Azure network interface.</span></span>

## <span data-ttu-id="9ea8d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9ea8d-107">EXAMPLES</span></span>

### <span data-ttu-id="9ea8d-108">Przykład 1: Usuwanie interfejsu sieciowego</span><span class="sxs-lookup"><span data-stu-id="9ea8d-108">Example 1: Remove a network interface</span></span>
```
PS C:\>Remove-AzureRmNetworkInterface -Name "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="9ea8d-109">To polecenie usuwa kartę Network Interface NetworkInterface1 w ResourceGroup1 Group (zasób).</span><span class="sxs-lookup"><span data-stu-id="9ea8d-109">This command removes the network interface NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="9ea8d-110">Ponieważ parametr *Force* nie jest wykorzystywany, użytkownik zostanie poproszony o potwierdzenie tej akcji.</span><span class="sxs-lookup"><span data-stu-id="9ea8d-110">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="9ea8d-111">Przykład 2: Usuwanie interfejsu sieciowego</span><span class="sxs-lookup"><span data-stu-id="9ea8d-111">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" | Remove-AzureRmNetworkInterface -Force
```

<span data-ttu-id="9ea8d-112">To polecenie usuwa wszystkie interfejsy sieciowe w ResourceGroup1 grup zasobów.</span><span class="sxs-lookup"><span data-stu-id="9ea8d-112">This command removes all network interfaces in resource group ResourceGroup1.</span></span>
<span data-ttu-id="9ea8d-113">Ponieważ parametr *Force* jest wykorzystywany, użytkownik nie jest monitowany o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9ea8d-113">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="9ea8d-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9ea8d-114">PARAMETERS</span></span>

### <span data-ttu-id="9ea8d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9ea8d-115">-AsJob</span></span>
<span data-ttu-id="9ea8d-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="9ea8d-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9ea8d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ea8d-117">-DefaultProfile</span></span>
<span data-ttu-id="9ea8d-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9ea8d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ea8d-119">-Force</span><span class="sxs-lookup"><span data-stu-id="9ea8d-119">-Force</span></span>
<span data-ttu-id="9ea8d-120">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="9ea8d-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9ea8d-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9ea8d-121">-Name</span></span>
<span data-ttu-id="9ea8d-122">Określa nazwę interfejsu sieciowego, który jest usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ea8d-122">Specifies the name of the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9ea8d-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9ea8d-123">-PassThru</span></span>
<span data-ttu-id="9ea8d-124">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="9ea8d-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9ea8d-125">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="9ea8d-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9ea8d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ea8d-126">-ResourceGroupName</span></span>
<span data-ttu-id="9ea8d-127">Określa nazwę grupy zasobów zawierającej interfejs sieciowy, który jest usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ea8d-127">Specifies the name of a resource group that contains the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9ea8d-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9ea8d-128">-Confirm</span></span>
<span data-ttu-id="9ea8d-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ea8d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ea8d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ea8d-130">-WhatIf</span></span>
<span data-ttu-id="9ea8d-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ea8d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ea8d-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9ea8d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ea8d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ea8d-133">CommonParameters</span></span>
<span data-ttu-id="9ea8d-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ea8d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ea8d-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ea8d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ea8d-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9ea8d-136">INPUTS</span></span>

## <span data-ttu-id="9ea8d-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9ea8d-137">OUTPUTS</span></span>

## <span data-ttu-id="9ea8d-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9ea8d-138">NOTES</span></span>

## <span data-ttu-id="9ea8d-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9ea8d-139">RELATED LINKS</span></span>

[<span data-ttu-id="9ea8d-140">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="9ea8d-140">Get-AzureRmNetworkInterface</span></span>](./Get-AzureRmNetworkInterface.md)

[<span data-ttu-id="9ea8d-141">Nowe — AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="9ea8d-141">New-AzureRmNetworkInterface</span></span>](./New-AzureRmNetworkInterface.md)

[<span data-ttu-id="9ea8d-142">Set-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="9ea8d-142">Set-AzureRmNetworkInterface</span></span>](./Set-AzureRmNetworkInterface.md)


