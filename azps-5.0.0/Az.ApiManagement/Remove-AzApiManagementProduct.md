---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D6B7F253-03CD-40BE-87D6-E4AE300A29D5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProduct.md
ms.openlocfilehash: 33b00df9e0c9c5b5e0ef04d22b745942535effcb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317352"
---
# <span data-ttu-id="2b4dd-101">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="2b4dd-101">Remove-AzApiManagementProduct</span></span>

## <span data-ttu-id="2b4dd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2b4dd-102">SYNOPSIS</span></span>
<span data-ttu-id="2b4dd-103">Usuwa istniejący produkt administracyjny API.</span><span class="sxs-lookup"><span data-stu-id="2b4dd-103">Removes an existing API Management product.</span></span>

## <span data-ttu-id="2b4dd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2b4dd-104">SYNTAX</span></span>

```
Remove-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b4dd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2b4dd-105">DESCRIPTION</span></span>
<span data-ttu-id="2b4dd-106">Polecenie cmdlet **Remove-AzApiManagementProduct** usuwa istniejący produkt administracyjny API.</span><span class="sxs-lookup"><span data-stu-id="2b4dd-106">The **Remove-AzApiManagementProduct** cmdlet removes an existing API Management product.</span></span>

## <span data-ttu-id="2b4dd-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2b4dd-107">EXAMPLES</span></span>

### <span data-ttu-id="2b4dd-108">Przykład 1: Usuwanie istniejącego produktu i wszystkich abonamentów</span><span class="sxs-lookup"><span data-stu-id="2b4dd-108">Example 1: Remove an existing product and all subscriptions</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -DeleteSubscriptions
```

<span data-ttu-id="2b4dd-109">To polecenie usuwa istniejący produkt i wszystkie abonamenty.</span><span class="sxs-lookup"><span data-stu-id="2b4dd-109">This command removes an existing product and all subscriptions.</span></span>

## <span data-ttu-id="2b4dd-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2b4dd-110">PARAMETERS</span></span>

### <span data-ttu-id="2b4dd-111">-Context</span><span class="sxs-lookup"><span data-stu-id="2b4dd-111">-Context</span></span>
<span data-ttu-id="2b4dd-112">Określa wystąpienie obiektu **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="2b4dd-112">Specifies an instance of the **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b4dd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b4dd-113">-DefaultProfile</span></span>
<span data-ttu-id="2b4dd-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2b4dd-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b4dd-115">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="2b4dd-115">-DeleteSubscriptions</span></span>
<span data-ttu-id="2b4dd-116">Wskazuje, czy należy usunąć abonamenty do produktu.</span><span class="sxs-lookup"><span data-stu-id="2b4dd-116">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="2b4dd-117">Jeśli nie ustawisz tego parametru i abonamentów, zostanie zgłoszony wyjątek.</span><span class="sxs-lookup"><span data-stu-id="2b4dd-117">If you do not set this parameter and subscriptions exists, an exception is thrown.</span></span>

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

### <span data-ttu-id="2b4dd-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2b4dd-118">-PassThru</span></span>
<span data-ttu-id="2b4dd-119">Wskazuje, że to polecenie cmdlet zwraca wartość $True, jeśli się powiodło, lub wartość $False, jeśli ta funkcja nie powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="2b4dd-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, if it fails.</span></span>

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

### <span data-ttu-id="2b4dd-120">-ProductId</span><span class="sxs-lookup"><span data-stu-id="2b4dd-120">-ProductId</span></span>
<span data-ttu-id="2b4dd-121">Określa identyfikator istniejącego produktu.</span><span class="sxs-lookup"><span data-stu-id="2b4dd-121">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="2b4dd-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2b4dd-122">-Confirm</span></span>
<span data-ttu-id="2b4dd-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b4dd-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b4dd-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b4dd-124">-WhatIf</span></span>
<span data-ttu-id="2b4dd-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b4dd-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b4dd-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2b4dd-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b4dd-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b4dd-127">CommonParameters</span></span>
<span data-ttu-id="2b4dd-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b4dd-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b4dd-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2b4dd-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b4dd-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2b4dd-130">INPUTS</span></span>

### <span data-ttu-id="2b4dd-131">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2b4dd-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2b4dd-132">System. String</span><span class="sxs-lookup"><span data-stu-id="2b4dd-132">System.String</span></span>

### <span data-ttu-id="2b4dd-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2b4dd-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2b4dd-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2b4dd-134">OUTPUTS</span></span>

### <span data-ttu-id="2b4dd-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2b4dd-135">System.Boolean</span></span>

## <span data-ttu-id="2b4dd-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2b4dd-136">NOTES</span></span>

## <span data-ttu-id="2b4dd-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2b4dd-137">RELATED LINKS</span></span>

[<span data-ttu-id="2b4dd-138">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="2b4dd-138">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="2b4dd-139">Nowe — AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="2b4dd-139">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="2b4dd-140">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="2b4dd-140">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)


