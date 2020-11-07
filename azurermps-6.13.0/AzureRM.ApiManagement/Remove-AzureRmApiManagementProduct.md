---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D6B7F253-03CD-40BE-87D6-E4AE300A29D5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProduct.md
ms.openlocfilehash: 61a4ab9e7a827cffce861cc9ebaf7382e16e8fcb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716800"
---
# <span data-ttu-id="838b1-101">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="838b1-101">Remove-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="838b1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="838b1-102">SYNOPSIS</span></span>
<span data-ttu-id="838b1-103">Usuwa istniejący produkt administracyjny API.</span><span class="sxs-lookup"><span data-stu-id="838b1-103">Removes an existing API Management product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="838b1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="838b1-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="838b1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="838b1-105">DESCRIPTION</span></span>
<span data-ttu-id="838b1-106">Polecenie cmdlet **Remove-AzureRmApiManagementProduct** usuwa istniejący produkt administracyjny API.</span><span class="sxs-lookup"><span data-stu-id="838b1-106">The **Remove-AzureRmApiManagementProduct** cmdlet removes an existing API Management product.</span></span>

## <span data-ttu-id="838b1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="838b1-107">EXAMPLES</span></span>

### <span data-ttu-id="838b1-108">Przykład 1: Usuwanie istniejącego produktu i wszystkich abonamentów</span><span class="sxs-lookup"><span data-stu-id="838b1-108">Example 1: Remove an existing product and all subscriptions</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementProduct -Context $apimContext -Id "0123456789" -DeleteSubscriptions -Force
```

<span data-ttu-id="838b1-109">To polecenie usuwa istniejący produkt i wszystkie abonamenty.</span><span class="sxs-lookup"><span data-stu-id="838b1-109">This command removes an existing product and all subscriptions.</span></span>

## <span data-ttu-id="838b1-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="838b1-110">PARAMETERS</span></span>

### <span data-ttu-id="838b1-111">-Context</span><span class="sxs-lookup"><span data-stu-id="838b1-111">-Context</span></span>
<span data-ttu-id="838b1-112">Określa wystąpienie obiektu **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="838b1-112">Specifies an instance of the **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="838b1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="838b1-113">-DefaultProfile</span></span>
<span data-ttu-id="838b1-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="838b1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="838b1-115">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="838b1-115">-DeleteSubscriptions</span></span>
<span data-ttu-id="838b1-116">Wskazuje, czy należy usunąć abonamenty do produktu.</span><span class="sxs-lookup"><span data-stu-id="838b1-116">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="838b1-117">Jeśli nie ustawisz tego parametru i abonamentów, zostanie zgłoszony wyjątek.</span><span class="sxs-lookup"><span data-stu-id="838b1-117">If you do not set this parameter and subscriptions exists, an exception is thrown.</span></span>

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

### <span data-ttu-id="838b1-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="838b1-118">-PassThru</span></span>
<span data-ttu-id="838b1-119">Wskazuje, że to polecenie cmdlet zwraca wartość $True, jeśli się powiodło, lub wartość $False, jeśli ta funkcja nie powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="838b1-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, if it fails.</span></span>

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

### <span data-ttu-id="838b1-120">-ProductId</span><span class="sxs-lookup"><span data-stu-id="838b1-120">-ProductId</span></span>
<span data-ttu-id="838b1-121">Określa identyfikator istniejącego produktu.</span><span class="sxs-lookup"><span data-stu-id="838b1-121">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="838b1-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="838b1-122">-Confirm</span></span>
<span data-ttu-id="838b1-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="838b1-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="838b1-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="838b1-124">-WhatIf</span></span>
<span data-ttu-id="838b1-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="838b1-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="838b1-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="838b1-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="838b1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="838b1-127">CommonParameters</span></span>
<span data-ttu-id="838b1-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="838b1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="838b1-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="838b1-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="838b1-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="838b1-130">INPUTS</span></span>

### <span data-ttu-id="838b1-131">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="838b1-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="838b1-132">System. String</span><span class="sxs-lookup"><span data-stu-id="838b1-132">System.String</span></span>

### <span data-ttu-id="838b1-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="838b1-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="838b1-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="838b1-134">OUTPUTS</span></span>

### <span data-ttu-id="838b1-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="838b1-135">System.Boolean</span></span>

## <span data-ttu-id="838b1-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="838b1-136">NOTES</span></span>

## <span data-ttu-id="838b1-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="838b1-137">RELATED LINKS</span></span>

[<span data-ttu-id="838b1-138">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="838b1-138">Get-AzureRmApiManagementProduct</span></span>](./Get-AzureRmApiManagementProduct.md)

[<span data-ttu-id="838b1-139">Nowe — AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="838b1-139">New-AzureRmApiManagementProduct</span></span>](./New-AzureRmApiManagementProduct.md)

[<span data-ttu-id="838b1-140">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="838b1-140">Set-AzureRmApiManagementProduct</span></span>](./Set-AzureRmApiManagementProduct.md)


