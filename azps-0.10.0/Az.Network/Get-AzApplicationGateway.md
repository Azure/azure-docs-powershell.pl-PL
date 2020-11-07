---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 77CDEE77-FD5D-4C2D-B027-FF1F6FF6618E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGateway.md
ms.openlocfilehash: 61547a4ee5f60fccc371ca7b2c426ca1a4bbb005
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890926"
---
# <span data-ttu-id="a812c-101">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a812c-101">Get-AzApplicationGateway</span></span>

## <span data-ttu-id="a812c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a812c-102">SYNOPSIS</span></span>
<span data-ttu-id="a812c-103">Pobiera bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a812c-103">Gets an application gateway.</span></span>

## <span data-ttu-id="a812c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a812c-104">SYNTAX</span></span>

```
Get-AzApplicationGateway [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a812c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a812c-105">DESCRIPTION</span></span>
<span data-ttu-id="a812c-106">Polecenie cmdlet **Get-AzApplicationGateway** pobiera bramę Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="a812c-106">The **Get-AzApplicationGateway** cmdlet gets an application gateway.</span></span>

## <span data-ttu-id="a812c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a812c-107">EXAMPLES</span></span>

### <span data-ttu-id="a812c-108">Przykład 1: uzyskiwanie określonej bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="a812c-108">Example 1: Get a specified application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="a812c-109">To polecenie pobiera bramkę Application Gateway o nazwie ApplicationGateway01 należącej do grupy zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="a812c-109">This command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

### <span data-ttu-id="a812c-110">Przykład 2: uzyskiwanie listy bram aplikacji w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="a812c-110">Example 2: Get a list of application gateways in a resource group</span></span>
```
PS C:\>$AppGwList = Get-AzApplicationGateway -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="a812c-111">To polecenie powoduje wyświetlenie listy wszystkich bram aplikacji w grupie zasób o nazwie ResourceGroup01 i zapisanie jej w zmiennej $AppGwList.</span><span class="sxs-lookup"><span data-stu-id="a812c-111">This command gets a list of all the application gateways in the resource group named ResourceGroup01 and stores it in the $AppGwList variable.</span></span>

### <span data-ttu-id="a812c-112">Przykład 3: uzyskiwanie listy bram aplikacji w subskrypcji</span><span class="sxs-lookup"><span data-stu-id="a812c-112">Example 3: Get a list of application gateways in a subscription</span></span>
```
PS C:\>$AppGwList = Get-AzApplicationGateway
```

<span data-ttu-id="a812c-113">To polecenie powoduje wyświetlenie listy wszystkich bram aplikacji w subskrypcji i zapisanie jej w zmiennej $AppGwList.</span><span class="sxs-lookup"><span data-stu-id="a812c-113">This command gets a list of all the application gateways in the subscription and stores it in the $AppGwList variable.</span></span>

## <span data-ttu-id="a812c-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a812c-114">PARAMETERS</span></span>

### <span data-ttu-id="a812c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a812c-115">-DefaultProfile</span></span>
<span data-ttu-id="a812c-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a812c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a812c-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a812c-117">-Name</span></span>
<span data-ttu-id="a812c-118">Określa nazwę bramy aplikacji, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a812c-118">Specifies the name of the application gateway that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a812c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a812c-119">-ResourceGroupName</span></span>
<span data-ttu-id="a812c-120">Określa nazwę grupy zasobów zawierającej bramkę Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="a812c-120">Specifies the name of the resource group that contains the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a812c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a812c-121">CommonParameters</span></span>
<span data-ttu-id="a812c-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a812c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a812c-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a812c-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a812c-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a812c-124">INPUTS</span></span>

### <span data-ttu-id="a812c-125">System. String</span><span class="sxs-lookup"><span data-stu-id="a812c-125">System.String</span></span>

## <span data-ttu-id="a812c-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a812c-126">OUTPUTS</span></span>

### <span data-ttu-id="a812c-127">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a812c-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a812c-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a812c-128">NOTES</span></span>

## <span data-ttu-id="a812c-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a812c-129">RELATED LINKS</span></span>

[<span data-ttu-id="a812c-130">Zatrzymaj — AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a812c-130">Stop-AzApplicationGateway</span></span>](./Stop-AzApplicationGateway.md)


