---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 1058BA4E-CD79-429D-BB05-422AE39230C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementproducttogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementProductToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementProductToGroup.md
ms.openlocfilehash: 2bed6664674894e84b88ae2d20092ad631010155
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707111"
---
# <span data-ttu-id="da45f-101">Add-AzApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="da45f-101">Add-AzApiManagementProductToGroup</span></span>

## <span data-ttu-id="da45f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="da45f-102">SYNOPSIS</span></span>
<span data-ttu-id="da45f-103">Dodaje produkt do grupy.</span><span class="sxs-lookup"><span data-stu-id="da45f-103">Adds a product to a group.</span></span>

## <span data-ttu-id="da45f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="da45f-104">SYNTAX</span></span>

```
Add-AzApiManagementProductToGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da45f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="da45f-105">DESCRIPTION</span></span>
<span data-ttu-id="da45f-106">Polecenie cmdlet **Add-AzApiManagementProductToGroup** umożliwia dodanie produktu do istniejącej grupy.</span><span class="sxs-lookup"><span data-stu-id="da45f-106">The **Add-AzApiManagementProductToGroup** cmdlet adds a product to an existing group.</span></span>
<span data-ttu-id="da45f-107">Innymi słowy, to polecenie cmdlet przypisuje grupę do produktu.</span><span class="sxs-lookup"><span data-stu-id="da45f-107">In other words, this cmdlet assigns a group to a product.</span></span>

## <span data-ttu-id="da45f-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="da45f-108">EXAMPLES</span></span>

### <span data-ttu-id="da45f-109">Przykład 1. Dodawanie produktu do grupy</span><span class="sxs-lookup"><span data-stu-id="da45f-109">Example 1: Add a product to a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementProductToGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="da45f-110">To polecenie umożliwia dodanie produktu do istniejącej grupy.</span><span class="sxs-lookup"><span data-stu-id="da45f-110">This command adds a product to an existing group.</span></span>

## <span data-ttu-id="da45f-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="da45f-111">PARAMETERS</span></span>

### <span data-ttu-id="da45f-112">-Context</span><span class="sxs-lookup"><span data-stu-id="da45f-112">-Context</span></span>
<span data-ttu-id="da45f-113">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="da45f-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="da45f-114">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="da45f-114">This parameter is required.</span></span>

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

### <span data-ttu-id="da45f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da45f-115">-DefaultProfile</span></span>
<span data-ttu-id="da45f-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="da45f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da45f-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="da45f-117">-GroupId</span></span>
<span data-ttu-id="da45f-118">Określa identyfikator grupy.</span><span class="sxs-lookup"><span data-stu-id="da45f-118">Specifies the group ID.</span></span>
<span data-ttu-id="da45f-119">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="da45f-119">This parameter is required.</span></span>

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

### <span data-ttu-id="da45f-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="da45f-120">-PassThru</span></span>
<span data-ttu-id="da45f-121">passthru</span><span class="sxs-lookup"><span data-stu-id="da45f-121">passthru</span></span>

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

### <span data-ttu-id="da45f-122">-ProductId</span><span class="sxs-lookup"><span data-stu-id="da45f-122">-ProductId</span></span>
<span data-ttu-id="da45f-123">Określa identyfikator produktu.</span><span class="sxs-lookup"><span data-stu-id="da45f-123">Specifies the product ID.</span></span>
<span data-ttu-id="da45f-124">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="da45f-124">This parameter is required.</span></span>

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

### <span data-ttu-id="da45f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da45f-125">CommonParameters</span></span>
<span data-ttu-id="da45f-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da45f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da45f-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="da45f-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da45f-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="da45f-128">INPUTS</span></span>

### <span data-ttu-id="da45f-129">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="da45f-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="da45f-130">System. String</span><span class="sxs-lookup"><span data-stu-id="da45f-130">System.String</span></span>

### <span data-ttu-id="da45f-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="da45f-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="da45f-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="da45f-132">OUTPUTS</span></span>

### <span data-ttu-id="da45f-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="da45f-133">System.Boolean</span></span>

## <span data-ttu-id="da45f-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="da45f-134">NOTES</span></span>

## <span data-ttu-id="da45f-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="da45f-135">RELATED LINKS</span></span>

[<span data-ttu-id="da45f-136">Remove-AzApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="da45f-136">Remove-AzApiManagementProductFromGroup</span></span>](./Remove-AzApiManagementProductFromGroup.md)


