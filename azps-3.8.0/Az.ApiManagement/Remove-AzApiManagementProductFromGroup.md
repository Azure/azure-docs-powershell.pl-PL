---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2FD2C5C0-5A5A-4CF0-9260-21B9E3DE52B9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementproductfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProductFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProductFromGroup.md
ms.openlocfilehash: a2afd2d5296912606363eddab49e0e3d6b371538
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051108"
---
# <span data-ttu-id="b8851-101">Remove-AzApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="b8851-101">Remove-AzApiManagementProductFromGroup</span></span>

## <span data-ttu-id="b8851-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b8851-102">SYNOPSIS</span></span>
<span data-ttu-id="b8851-103">Usuwa produkt z grupy.</span><span class="sxs-lookup"><span data-stu-id="b8851-103">Removes a product from a group.</span></span>

## <span data-ttu-id="b8851-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b8851-104">SYNTAX</span></span>

```
Remove-AzApiManagementProductFromGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8851-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b8851-105">DESCRIPTION</span></span>
<span data-ttu-id="b8851-106">Polecenie cmdlet **Remove-AzApiManagementProductFromGroup** usuwa produkt z istniejącej grupy.</span><span class="sxs-lookup"><span data-stu-id="b8851-106">The **Remove-AzApiManagementProductFromGroup** cmdlet removes a product from an existing group.</span></span>
<span data-ttu-id="b8851-107">Innymi słowy, to polecenie cmdlet Usuwa przypisanie grupy z produktu.</span><span class="sxs-lookup"><span data-stu-id="b8851-107">In other words, this cmdlet removes the group assignment from a product.</span></span>

## <span data-ttu-id="b8851-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b8851-108">EXAMPLES</span></span>

### <span data-ttu-id="b8851-109">Przykład 1: usuwanie produktu z grupy</span><span class="sxs-lookup"><span data-stu-id="b8851-109">Example 1: Remove a product from a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementProductFromGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="b8851-110">To polecenie umożliwia usunięcie produktu z istniejącej grupy.</span><span class="sxs-lookup"><span data-stu-id="b8851-110">This command removes a product from an existing group.</span></span>

## <span data-ttu-id="b8851-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b8851-111">PARAMETERS</span></span>

### <span data-ttu-id="b8851-112">-Context</span><span class="sxs-lookup"><span data-stu-id="b8851-112">-Context</span></span>
<span data-ttu-id="b8851-113">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="b8851-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="b8851-114">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="b8851-114">This parameter is required.</span></span>

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

### <span data-ttu-id="b8851-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8851-115">-DefaultProfile</span></span>
<span data-ttu-id="b8851-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b8851-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8851-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="b8851-117">-GroupId</span></span>
<span data-ttu-id="b8851-118">Określa identyfikator grupy.</span><span class="sxs-lookup"><span data-stu-id="b8851-118">Specifies the group ID.</span></span>
<span data-ttu-id="b8851-119">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="b8851-119">This parameter is required.</span></span>

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

### <span data-ttu-id="b8851-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b8851-120">-PassThru</span></span>
<span data-ttu-id="b8851-121">Wskazuje, że to polecenie cmdlet zwraca wartość $True, jeśli się powiedzie lub $False, w przeciwnym razie.</span><span class="sxs-lookup"><span data-stu-id="b8851-121">Indicates that this cmdlet returns a value of $True, if it succeeds, or $False, otherwise.</span></span>

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

### <span data-ttu-id="b8851-122">-ProductId</span><span class="sxs-lookup"><span data-stu-id="b8851-122">-ProductId</span></span>
<span data-ttu-id="b8851-123">Określa identyfikator produktu.</span><span class="sxs-lookup"><span data-stu-id="b8851-123">Specifies the product ID.</span></span>
<span data-ttu-id="b8851-124">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="b8851-124">This parameter is required.</span></span>

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

### <span data-ttu-id="b8851-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8851-125">CommonParameters</span></span>
<span data-ttu-id="b8851-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8851-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8851-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b8851-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8851-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b8851-128">INPUTS</span></span>

### <span data-ttu-id="b8851-129">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b8851-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b8851-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b8851-130">System.String</span></span>

### <span data-ttu-id="b8851-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b8851-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b8851-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b8851-132">OUTPUTS</span></span>

### <span data-ttu-id="b8851-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b8851-133">System.Boolean</span></span>

## <span data-ttu-id="b8851-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b8851-134">NOTES</span></span>

## <span data-ttu-id="b8851-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b8851-135">RELATED LINKS</span></span>

[<span data-ttu-id="b8851-136">Dodaj-AzApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="b8851-136">Add-AzApiManagementProductToGroup</span></span>](./Add-AzApiManagementProductToGroup.md)


