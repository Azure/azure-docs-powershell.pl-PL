---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 78BADAF3-6001-4A25-A74D-F6B50079FCB4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 1c51d58d7732a3f9d07f1beba24a7584b35733b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546188"
---
# <span data-ttu-id="26b20-101">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="26b20-101">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="26b20-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="26b20-102">SYNOPSIS</span></span>
<span data-ttu-id="26b20-103">Konfiguruje klucz udostępniony połączenia bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="26b20-103">Configures the shared key of the virtual network gateway connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26b20-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="26b20-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -Value <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26b20-105">Opis</span><span class="sxs-lookup"><span data-stu-id="26b20-105">DESCRIPTION</span></span>
<span data-ttu-id="26b20-106">Polecenie cmdlet **Set-AzureRmVirtualNetworkGatewayConnectionSharedKey** konfiguruje klucz współużytkowany połączenia bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="26b20-106">The **Set-AzureRmVirtualNetworkGatewayConnectionSharedKey** cmdlet configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="26b20-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="26b20-107">EXAMPLES</span></span>

## <span data-ttu-id="26b20-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="26b20-108">PARAMETERS</span></span>

### <span data-ttu-id="26b20-109">-Force</span><span class="sxs-lookup"><span data-stu-id="26b20-109">-Force</span></span>
<span data-ttu-id="26b20-110">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="26b20-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="26b20-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="26b20-111">-Name</span></span>
<span data-ttu-id="26b20-112">Określa nazwę klucza udostępnionego bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="26b20-112">Specifies the name of the virtual network gateway shared key.</span></span>

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

### <span data-ttu-id="26b20-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26b20-113">-ResourceGroupName</span></span>
<span data-ttu-id="26b20-114">Określa nazwę grupy zasobów, do której należy Brama sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="26b20-114">Specifies the name of the resource group that the virtual network gateway belongs to</span></span>

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

### <span data-ttu-id="26b20-115">-Value</span><span class="sxs-lookup"><span data-stu-id="26b20-115">-Value</span></span>
<span data-ttu-id="26b20-116">Określa wartość klucza udostępnionego.</span><span class="sxs-lookup"><span data-stu-id="26b20-116">Specifies the value of the shared key.</span></span>

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

### <span data-ttu-id="26b20-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="26b20-117">-Confirm</span></span>
<span data-ttu-id="26b20-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26b20-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26b20-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26b20-119">-WhatIf</span></span>
<span data-ttu-id="26b20-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26b20-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26b20-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="26b20-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26b20-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26b20-122">-DefaultProfile</span></span>
<span data-ttu-id="26b20-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="26b20-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26b20-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26b20-124">CommonParameters</span></span>
<span data-ttu-id="26b20-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26b20-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26b20-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26b20-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26b20-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="26b20-127">INPUTS</span></span>

## <span data-ttu-id="26b20-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="26b20-128">OUTPUTS</span></span>

### <span data-ttu-id="26b20-129">System. String</span><span class="sxs-lookup"><span data-stu-id="26b20-129">System.String</span></span>

## <span data-ttu-id="26b20-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="26b20-130">NOTES</span></span>

## <span data-ttu-id="26b20-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="26b20-131">RELATED LINKS</span></span>

[<span data-ttu-id="26b20-132">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="26b20-132">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="26b20-133">Resetowanie — AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="26b20-133">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)


