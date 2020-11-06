---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 1058BA4E-CD79-429D-BB05-422AE39230C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/add-azurermapimanagementproducttogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementProductToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementProductToGroup.md
ms.openlocfilehash: 1bd1027c0d58f1ee38ca23c28b3021bdc2b95d19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526422"
---
# <span data-ttu-id="50192-101">Add-AzureRmApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="50192-101">Add-AzureRmApiManagementProductToGroup</span></span>

## <span data-ttu-id="50192-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="50192-102">SYNOPSIS</span></span>
<span data-ttu-id="50192-103">Dodaje produkt do grupy.</span><span class="sxs-lookup"><span data-stu-id="50192-103">Adds a product to a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50192-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="50192-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementProductToGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50192-105">Opis</span><span class="sxs-lookup"><span data-stu-id="50192-105">DESCRIPTION</span></span>
<span data-ttu-id="50192-106">Polecenie cmdlet **Add-AzureRmApiManagementProductToGroup** umożliwia dodanie produktu do istniejącej grupy.</span><span class="sxs-lookup"><span data-stu-id="50192-106">The **Add-AzureRmApiManagementProductToGroup** cmdlet adds a product to an existing group.</span></span>
<span data-ttu-id="50192-107">Innymi słowy, to polecenie cmdlet przypisuje grupę do produktu.</span><span class="sxs-lookup"><span data-stu-id="50192-107">In other words, this cmdlet assigns a group to a product.</span></span>

## <span data-ttu-id="50192-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="50192-108">EXAMPLES</span></span>

### <span data-ttu-id="50192-109">Przykład 1. Dodawanie produktu do grupy</span><span class="sxs-lookup"><span data-stu-id="50192-109">Example 1: Add a product to a group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzureRmApiManagementProductToGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="50192-110">To polecenie umożliwia dodanie produktu do istniejącej grupy.</span><span class="sxs-lookup"><span data-stu-id="50192-110">This command adds a product to an existing group.</span></span>

## <span data-ttu-id="50192-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="50192-111">PARAMETERS</span></span>

### <span data-ttu-id="50192-112">-Context</span><span class="sxs-lookup"><span data-stu-id="50192-112">-Context</span></span>
<span data-ttu-id="50192-113">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="50192-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="50192-114">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="50192-114">This parameter is required.</span></span>

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

### <span data-ttu-id="50192-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50192-115">-DefaultProfile</span></span>
<span data-ttu-id="50192-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="50192-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50192-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="50192-117">-GroupId</span></span>
<span data-ttu-id="50192-118">Określa identyfikator grupy.</span><span class="sxs-lookup"><span data-stu-id="50192-118">Specifies the group ID.</span></span>
<span data-ttu-id="50192-119">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="50192-119">This parameter is required.</span></span>

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

### <span data-ttu-id="50192-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="50192-120">-PassThru</span></span>
<span data-ttu-id="50192-121">passthru</span><span class="sxs-lookup"><span data-stu-id="50192-121">passthru</span></span>

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

### <span data-ttu-id="50192-122">-ProductId</span><span class="sxs-lookup"><span data-stu-id="50192-122">-ProductId</span></span>
<span data-ttu-id="50192-123">Określa identyfikator produktu.</span><span class="sxs-lookup"><span data-stu-id="50192-123">Specifies the product ID.</span></span>
<span data-ttu-id="50192-124">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="50192-124">This parameter is required.</span></span>

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

### <span data-ttu-id="50192-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50192-125">CommonParameters</span></span>
<span data-ttu-id="50192-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50192-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50192-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50192-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50192-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="50192-128">INPUTS</span></span>

### <span data-ttu-id="50192-129">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="50192-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="50192-130">System. String</span><span class="sxs-lookup"><span data-stu-id="50192-130">System.String</span></span>

### <span data-ttu-id="50192-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="50192-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="50192-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="50192-132">OUTPUTS</span></span>

### <span data-ttu-id="50192-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="50192-133">System.Boolean</span></span>

## <span data-ttu-id="50192-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="50192-134">NOTES</span></span>

## <span data-ttu-id="50192-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="50192-135">RELATED LINKS</span></span>

[<span data-ttu-id="50192-136">Remove-AzureRmApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="50192-136">Remove-AzureRmApiManagementProductFromGroup</span></span>](./Remove-AzureRmApiManagementProductFromGroup.md)


