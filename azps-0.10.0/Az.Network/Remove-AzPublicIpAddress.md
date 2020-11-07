---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 00236BC2-61D8-49C2-91BE-923C567153F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzPublicIpAddress.md
ms.openlocfilehash: 299e27d0d4824dfe06a6f1982f4eda1a04eeb1c4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892933"
---
# <span data-ttu-id="d46fe-101">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d46fe-101">Remove-AzPublicIpAddress</span></span>

## <span data-ttu-id="d46fe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d46fe-102">SYNOPSIS</span></span>
<span data-ttu-id="d46fe-103">Usuwa publiczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="d46fe-103">Removes a public IP address.</span></span>

## <span data-ttu-id="d46fe-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d46fe-104">SYNTAX</span></span>

```
Remove-AzPublicIpAddress -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d46fe-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d46fe-105">DESCRIPTION</span></span>
<span data-ttu-id="d46fe-106">Polecenie cmdlet **Remove-AzPublicIpAddress** usuwa publiczny adres IP platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d46fe-106">The **Remove-AzPublicIpAddress** cmdlet removes an Azure public IP address.</span></span>

## <span data-ttu-id="d46fe-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d46fe-107">EXAMPLES</span></span>

### <span data-ttu-id="d46fe-108">1: usuwanie zasobu publicznego adresu IP</span><span class="sxs-lookup"><span data-stu-id="d46fe-108">1: Remove a public IP address resource</span></span>
```
Remove-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="d46fe-109">To polecenie usuwa zasób publiczny adres IP o nazwie $publicIpName w grupie zasób $rgName.</span><span class="sxs-lookup"><span data-stu-id="d46fe-109">This command removes the public IP address resource named $publicIpName in the resource group $rgName.</span></span>

## <span data-ttu-id="d46fe-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d46fe-110">PARAMETERS</span></span>

### <span data-ttu-id="d46fe-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d46fe-111">-AsJob</span></span>
<span data-ttu-id="d46fe-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d46fe-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d46fe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d46fe-113">-DefaultProfile</span></span>
<span data-ttu-id="d46fe-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d46fe-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d46fe-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d46fe-115">-Force</span></span>
<span data-ttu-id="d46fe-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="d46fe-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d46fe-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d46fe-117">-Name</span></span>
<span data-ttu-id="d46fe-118">Określa nazwę publicznego adresu IP, który jest usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d46fe-118">Specifies the name of the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d46fe-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d46fe-119">-PassThru</span></span>
<span data-ttu-id="d46fe-120">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="d46fe-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d46fe-121">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="d46fe-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d46fe-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d46fe-122">-ResourceGroupName</span></span>
<span data-ttu-id="d46fe-123">Określa nazwę grupy zasobów zawierającej publiczny adres IP, który jest usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d46fe-123">Specifies the name of the resource group that contains the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d46fe-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d46fe-124">-Confirm</span></span>
<span data-ttu-id="d46fe-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d46fe-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d46fe-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d46fe-126">-WhatIf</span></span>
<span data-ttu-id="d46fe-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d46fe-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d46fe-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d46fe-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d46fe-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d46fe-129">CommonParameters</span></span>
<span data-ttu-id="d46fe-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d46fe-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d46fe-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d46fe-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d46fe-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d46fe-132">INPUTS</span></span>

## <span data-ttu-id="d46fe-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d46fe-133">OUTPUTS</span></span>

## <span data-ttu-id="d46fe-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d46fe-134">NOTES</span></span>

## <span data-ttu-id="d46fe-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d46fe-135">RELATED LINKS</span></span>

[<span data-ttu-id="d46fe-136">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d46fe-136">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="d46fe-137">Nowe — AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d46fe-137">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="d46fe-138">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d46fe-138">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)


