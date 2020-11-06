---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 2FD2C5C0-5A5A-4CF0-9260-21B9E3DE52B9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementproductfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProductFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProductFromGroup.md
ms.openlocfilehash: 2eba88e94cfed3c253a5b5febc20a7585ab096d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525398"
---
# <span data-ttu-id="336f9-101">Remove-AzureRmApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="336f9-101">Remove-AzureRmApiManagementProductFromGroup</span></span>

## <span data-ttu-id="336f9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="336f9-102">SYNOPSIS</span></span>
<span data-ttu-id="336f9-103">Usuwa produkt z grupy.</span><span class="sxs-lookup"><span data-stu-id="336f9-103">Removes a product from a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="336f9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="336f9-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementProductFromGroup -Context <PsApiManagementContext> -GroupId <String>
 -ProductId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="336f9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="336f9-105">DESCRIPTION</span></span>
<span data-ttu-id="336f9-106">Polecenie cmdlet **Remove-AzureRmApiManagementProductFromGroup** usuwa produkt z istniejącej grupy.</span><span class="sxs-lookup"><span data-stu-id="336f9-106">The **Remove-AzureRmApiManagementProductFromGroup** cmdlet removes a product from an existing group.</span></span>
<span data-ttu-id="336f9-107">Innymi słowy, to polecenie cmdlet Usuwa przypisanie grupy z produktu.</span><span class="sxs-lookup"><span data-stu-id="336f9-107">In other words, this cmdlet removes the group assignment from a product.</span></span>

## <span data-ttu-id="336f9-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="336f9-108">EXAMPLES</span></span>

### <span data-ttu-id="336f9-109">Przykład 1: usuwanie produktu z grupy</span><span class="sxs-lookup"><span data-stu-id="336f9-109">Example 1: Remove a product from a group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementProductFromGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="336f9-110">To polecenie umożliwia usunięcie produktu z istniejącej grupy.</span><span class="sxs-lookup"><span data-stu-id="336f9-110">This command removes a product from an existing group.</span></span>

## <span data-ttu-id="336f9-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="336f9-111">PARAMETERS</span></span>

### <span data-ttu-id="336f9-112">-Context</span><span class="sxs-lookup"><span data-stu-id="336f9-112">-Context</span></span>
<span data-ttu-id="336f9-113">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="336f9-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="336f9-114">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="336f9-114">This parameter is required.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="336f9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="336f9-115">-DefaultProfile</span></span>
<span data-ttu-id="336f9-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="336f9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="336f9-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="336f9-117">-GroupId</span></span>
<span data-ttu-id="336f9-118">Określa identyfikator grupy.</span><span class="sxs-lookup"><span data-stu-id="336f9-118">Specifies the group ID.</span></span>
<span data-ttu-id="336f9-119">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="336f9-119">This parameter is required.</span></span>

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

### <span data-ttu-id="336f9-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="336f9-120">-PassThru</span></span>
<span data-ttu-id="336f9-121">Wskazuje, że to polecenie cmdlet zwraca wartość $True, jeśli się powiedzie lub $False, w przeciwnym razie.</span><span class="sxs-lookup"><span data-stu-id="336f9-121">Indicates that this cmdlet returns a value of $True, if it succeeds, or $False, otherwise.</span></span>

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

### <span data-ttu-id="336f9-122">-ProductId</span><span class="sxs-lookup"><span data-stu-id="336f9-122">-ProductId</span></span>
<span data-ttu-id="336f9-123">Określa identyfikator produktu.</span><span class="sxs-lookup"><span data-stu-id="336f9-123">Specifies the product ID.</span></span>
<span data-ttu-id="336f9-124">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="336f9-124">This parameter is required.</span></span>

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

### <span data-ttu-id="336f9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="336f9-125">CommonParameters</span></span>
<span data-ttu-id="336f9-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="336f9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="336f9-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="336f9-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="336f9-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="336f9-128">INPUTS</span></span>

### <span data-ttu-id="336f9-129">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="336f9-129">None</span></span>
<span data-ttu-id="336f9-130">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="336f9-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="336f9-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="336f9-131">OUTPUTS</span></span>

### <span data-ttu-id="336f9-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="336f9-132">System.Boolean</span></span>

## <span data-ttu-id="336f9-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="336f9-133">NOTES</span></span>

## <span data-ttu-id="336f9-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="336f9-134">RELATED LINKS</span></span>

[<span data-ttu-id="336f9-135">Dodaj-AzureRmApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="336f9-135">Add-AzureRmApiManagementProductToGroup</span></span>](./Add-AzureRmApiManagementProductToGroup.md)


