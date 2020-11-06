---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 00236BC2-61D8-49C2-91BE-923C567153F3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmPublicIpAddress.md
ms.openlocfilehash: 396f603c4a4126b8d438f0048677da7a5dbd7492
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546207"
---
# <span data-ttu-id="3a282-101">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="3a282-101">Remove-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="3a282-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3a282-102">SYNOPSIS</span></span>
<span data-ttu-id="3a282-103">Usuwa publiczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="3a282-103">Removes a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a282-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3a282-104">SYNTAX</span></span>

```
Remove-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a282-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3a282-105">DESCRIPTION</span></span>
<span data-ttu-id="3a282-106">Polecenie cmdlet **Remove-AzureRmPublicIpAddress** usuwa publiczny adres IP platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3a282-106">The **Remove-AzureRmPublicIpAddress** cmdlet removes an Azure public IP address.</span></span>

## <span data-ttu-id="3a282-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3a282-107">EXAMPLES</span></span>

### <span data-ttu-id="3a282-108">1: usuwanie zasobu publicznego adresu IP</span><span class="sxs-lookup"><span data-stu-id="3a282-108">1: Remove a public IP address resource</span></span>
```
Remove-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="3a282-109">To polecenie usuwa zasób publiczny adres IP o nazwie $publicIpName w grupie zasób $rgName.</span><span class="sxs-lookup"><span data-stu-id="3a282-109">This command removes the public IP address resource named $publicIpName in the resource group $rgName.</span></span>

## <span data-ttu-id="3a282-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3a282-110">PARAMETERS</span></span>

### <span data-ttu-id="3a282-111">-Force</span><span class="sxs-lookup"><span data-stu-id="3a282-111">-Force</span></span>
<span data-ttu-id="3a282-112">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="3a282-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3a282-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3a282-113">-Name</span></span>
<span data-ttu-id="3a282-114">Określa nazwę publicznego adresu IP, który jest usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a282-114">Specifies the name of the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3a282-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3a282-115">-PassThru</span></span>
<span data-ttu-id="3a282-116">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="3a282-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3a282-117">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="3a282-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3a282-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a282-118">-ResourceGroupName</span></span>
<span data-ttu-id="3a282-119">Określa nazwę grupy zasobów zawierającej publiczny adres IP, który jest usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a282-119">Specifies the name of the resource group that contains the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3a282-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3a282-120">-Confirm</span></span>
<span data-ttu-id="3a282-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a282-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a282-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a282-122">-WhatIf</span></span>
<span data-ttu-id="3a282-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a282-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a282-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3a282-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a282-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a282-125">-DefaultProfile</span></span>
<span data-ttu-id="3a282-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3a282-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a282-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a282-127">CommonParameters</span></span>
<span data-ttu-id="3a282-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a282-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a282-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a282-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a282-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3a282-130">INPUTS</span></span>

## <span data-ttu-id="3a282-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3a282-131">OUTPUTS</span></span>

## <span data-ttu-id="3a282-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3a282-132">NOTES</span></span>

## <span data-ttu-id="3a282-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3a282-133">RELATED LINKS</span></span>

[<span data-ttu-id="3a282-134">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="3a282-134">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="3a282-135">Nowe — AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="3a282-135">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="3a282-136">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="3a282-136">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)


