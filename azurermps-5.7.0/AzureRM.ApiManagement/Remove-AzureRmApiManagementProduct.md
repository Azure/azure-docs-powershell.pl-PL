---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: D6B7F253-03CD-40BE-87D6-E4AE300A29D5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProduct.md
ms.openlocfilehash: 5c5bd7d0b7df385645bdb51d684616f2c0d7eaa5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525397"
---
# <span data-ttu-id="13bd5-101">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="13bd5-101">Remove-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="13bd5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="13bd5-102">SYNOPSIS</span></span>
<span data-ttu-id="13bd5-103">Usuwa istniejący produkt administracyjny API.</span><span class="sxs-lookup"><span data-stu-id="13bd5-103">Removes an existing API Management product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13bd5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="13bd5-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13bd5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="13bd5-105">DESCRIPTION</span></span>
<span data-ttu-id="13bd5-106">Polecenie cmdlet **Remove-AzureRmApiManagementProduct** usuwa istniejący produkt administracyjny API.</span><span class="sxs-lookup"><span data-stu-id="13bd5-106">The **Remove-AzureRmApiManagementProduct** cmdlet removes an existing API Management product.</span></span>

## <span data-ttu-id="13bd5-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="13bd5-107">EXAMPLES</span></span>

### <span data-ttu-id="13bd5-108">Przykład 1: Usuwanie istniejącego produktu i wszystkich abonamentów</span><span class="sxs-lookup"><span data-stu-id="13bd5-108">Example 1: Remove an existing product and all subscriptions</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementProduct -Context $apimContext -Id "0123456789" -DeleteSubscriptions -Force
```

<span data-ttu-id="13bd5-109">To polecenie usuwa istniejący produkt i wszystkie abonamenty.</span><span class="sxs-lookup"><span data-stu-id="13bd5-109">This command removes an existing product and all subscriptions.</span></span>

## <span data-ttu-id="13bd5-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="13bd5-110">PARAMETERS</span></span>

### <span data-ttu-id="13bd5-111">-Context</span><span class="sxs-lookup"><span data-stu-id="13bd5-111">-Context</span></span>
<span data-ttu-id="13bd5-112">Określa wystąpienie obiektu **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="13bd5-112">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="13bd5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13bd5-113">-DefaultProfile</span></span>
<span data-ttu-id="13bd5-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="13bd5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="13bd5-115">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="13bd5-115">-DeleteSubscriptions</span></span>
<span data-ttu-id="13bd5-116">Wskazuje, czy należy usunąć abonamenty do produktu.</span><span class="sxs-lookup"><span data-stu-id="13bd5-116">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="13bd5-117">Jeśli nie ustawisz tego parametru i abonamentów, zostanie zgłoszony wyjątek.</span><span class="sxs-lookup"><span data-stu-id="13bd5-117">If you do not set this parameter and subscriptions exists, an exception is thrown.</span></span>

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

### <span data-ttu-id="13bd5-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="13bd5-118">-PassThru</span></span>
<span data-ttu-id="13bd5-119">Wskazuje, że to polecenie cmdlet zwraca wartość $True, jeśli się powiodło, lub wartość $False, jeśli ta funkcja nie powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="13bd5-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, if it fails.</span></span>

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

### <span data-ttu-id="13bd5-120">-ProductId</span><span class="sxs-lookup"><span data-stu-id="13bd5-120">-ProductId</span></span>
<span data-ttu-id="13bd5-121">Określa identyfikator istniejącego produktu.</span><span class="sxs-lookup"><span data-stu-id="13bd5-121">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="13bd5-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="13bd5-122">-Confirm</span></span>
<span data-ttu-id="13bd5-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13bd5-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13bd5-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13bd5-124">-WhatIf</span></span>
<span data-ttu-id="13bd5-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13bd5-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13bd5-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="13bd5-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13bd5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13bd5-127">CommonParameters</span></span>
<span data-ttu-id="13bd5-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13bd5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13bd5-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13bd5-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13bd5-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="13bd5-130">INPUTS</span></span>

### <span data-ttu-id="13bd5-131">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="13bd5-131">None</span></span>
<span data-ttu-id="13bd5-132">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="13bd5-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="13bd5-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="13bd5-133">OUTPUTS</span></span>

### <span data-ttu-id="13bd5-134">logiczną</span><span class="sxs-lookup"><span data-stu-id="13bd5-134">bool</span></span>

## <span data-ttu-id="13bd5-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="13bd5-135">NOTES</span></span>

## <span data-ttu-id="13bd5-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="13bd5-136">RELATED LINKS</span></span>

[<span data-ttu-id="13bd5-137">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="13bd5-137">Get-AzureRmApiManagementProduct</span></span>](./Get-AzureRmApiManagementProduct.md)

[<span data-ttu-id="13bd5-138">Nowe — AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="13bd5-138">New-AzureRmApiManagementProduct</span></span>](./New-AzureRmApiManagementProduct.md)

[<span data-ttu-id="13bd5-139">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="13bd5-139">Set-AzureRmApiManagementProduct</span></span>](./Set-AzureRmApiManagementProduct.md)


