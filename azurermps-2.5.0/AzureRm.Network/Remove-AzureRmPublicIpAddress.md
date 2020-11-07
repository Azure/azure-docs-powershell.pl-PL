---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 00236BC2-61D8-49C2-91BE-923C567153F3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermpublicipaddress
schema: 2.0.0
ms.openlocfilehash: af8a85c698a59a31516c6dee05bb57415a45ff62
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898254"
---
# <span data-ttu-id="3da4e-101">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="3da4e-101">Remove-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="3da4e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3da4e-102">SYNOPSIS</span></span>
<span data-ttu-id="3da4e-103">Usuwa publiczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="3da4e-103">Removes a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3da4e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3da4e-104">SYNTAX</span></span>

```
Remove-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3da4e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3da4e-105">DESCRIPTION</span></span>
<span data-ttu-id="3da4e-106">Polecenie cmdlet **Remove-AzureRmPublicIpAddress** usuwa publiczny adres IP platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3da4e-106">The **Remove-AzureRmPublicIpAddress** cmdlet removes an Azure public IP address.</span></span>

## <span data-ttu-id="3da4e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3da4e-107">EXAMPLES</span></span>

### <span data-ttu-id="3da4e-108">1: usuwanie zasobu publicznego adresu IP</span><span class="sxs-lookup"><span data-stu-id="3da4e-108">1: Remove a public IP address resource</span></span>
```
Remove-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="3da4e-109">To polecenie usuwa zasób publiczny adres IP o nazwie $publicIpName w grupie zasób $rgName.</span><span class="sxs-lookup"><span data-stu-id="3da4e-109">This command removes the public IP address resource named $publicIpName in the resource group $rgName.</span></span>

## <span data-ttu-id="3da4e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3da4e-110">PARAMETERS</span></span>

### <span data-ttu-id="3da4e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3da4e-111">-AsJob</span></span>
<span data-ttu-id="3da4e-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="3da4e-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3da4e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3da4e-113">-DefaultProfile</span></span>
<span data-ttu-id="3da4e-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3da4e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3da4e-115">-Force</span><span class="sxs-lookup"><span data-stu-id="3da4e-115">-Force</span></span>
<span data-ttu-id="3da4e-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="3da4e-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3da4e-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3da4e-117">-Name</span></span>
<span data-ttu-id="3da4e-118">Określa nazwę publicznego adresu IP, który jest usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3da4e-118">Specifies the name of the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3da4e-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3da4e-119">-PassThru</span></span>
<span data-ttu-id="3da4e-120">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="3da4e-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3da4e-121">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="3da4e-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3da4e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3da4e-122">-ResourceGroupName</span></span>
<span data-ttu-id="3da4e-123">Określa nazwę grupy zasobów zawierającej publiczny adres IP, który jest usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3da4e-123">Specifies the name of the resource group that contains the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3da4e-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3da4e-124">-Confirm</span></span>
<span data-ttu-id="3da4e-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3da4e-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3da4e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3da4e-126">-WhatIf</span></span>
<span data-ttu-id="3da4e-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3da4e-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3da4e-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3da4e-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3da4e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3da4e-129">CommonParameters</span></span>
<span data-ttu-id="3da4e-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3da4e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3da4e-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3da4e-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3da4e-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3da4e-132">INPUTS</span></span>

## <span data-ttu-id="3da4e-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3da4e-133">OUTPUTS</span></span>

## <span data-ttu-id="3da4e-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3da4e-134">NOTES</span></span>

## <span data-ttu-id="3da4e-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3da4e-135">RELATED LINKS</span></span>

[<span data-ttu-id="3da4e-136">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="3da4e-136">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="3da4e-137">Nowe — AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="3da4e-137">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="3da4e-138">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="3da4e-138">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)


