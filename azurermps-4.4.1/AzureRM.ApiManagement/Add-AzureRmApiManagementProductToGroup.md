---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 1058BA4E-CD79-429D-BB05-422AE39230C4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementProductToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementProductToGroup.md
ms.openlocfilehash: b4e1a029eca4e7eda48f44d85292639767eaf845
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550140"
---
# <span data-ttu-id="d7a21-101">Add-AzureRmApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="d7a21-101">Add-AzureRmApiManagementProductToGroup</span></span>

## <span data-ttu-id="d7a21-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d7a21-102">SYNOPSIS</span></span>
<span data-ttu-id="d7a21-103">Dodaje produkt do grupy.</span><span class="sxs-lookup"><span data-stu-id="d7a21-103">Adds a product to a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7a21-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d7a21-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementProductToGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7a21-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d7a21-105">DESCRIPTION</span></span>
<span data-ttu-id="d7a21-106">Polecenie cmdlet **Add-AzureRmApiManagementProductToGroup** umożliwia dodanie produktu do istniejącej grupy.</span><span class="sxs-lookup"><span data-stu-id="d7a21-106">The **Add-AzureRmApiManagementProductToGroup** cmdlet adds a product to an existing group.</span></span>
<span data-ttu-id="d7a21-107">Innymi słowy, to polecenie cmdlet przypisuje grupę do produktu.</span><span class="sxs-lookup"><span data-stu-id="d7a21-107">In other words, this cmdlet assigns a group to a product.</span></span>

## <span data-ttu-id="d7a21-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d7a21-108">EXAMPLES</span></span>

### <span data-ttu-id="d7a21-109">Przykład 1. Dodawanie produktu do grupy</span><span class="sxs-lookup"><span data-stu-id="d7a21-109">Example 1: Add a product to a group</span></span>
```
PS C:\>Add-AzureRmApiManagementProductToGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="d7a21-110">To polecenie umożliwia dodanie produktu do istniejącej grupy.</span><span class="sxs-lookup"><span data-stu-id="d7a21-110">This command adds a product to an existing group.</span></span>

## <span data-ttu-id="d7a21-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d7a21-111">PARAMETERS</span></span>

### <span data-ttu-id="d7a21-112">-Context</span><span class="sxs-lookup"><span data-stu-id="d7a21-112">-Context</span></span>
<span data-ttu-id="d7a21-113">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="d7a21-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="d7a21-114">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="d7a21-114">This parameter is required.</span></span>

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

### <span data-ttu-id="d7a21-115">-GroupId</span><span class="sxs-lookup"><span data-stu-id="d7a21-115">-GroupId</span></span>
<span data-ttu-id="d7a21-116">Określa identyfikator grupy.</span><span class="sxs-lookup"><span data-stu-id="d7a21-116">Specifies the group ID.</span></span>
<span data-ttu-id="d7a21-117">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="d7a21-117">This parameter is required.</span></span>

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

### <span data-ttu-id="d7a21-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d7a21-118">-PassThru</span></span>
<span data-ttu-id="d7a21-119">passthru</span><span class="sxs-lookup"><span data-stu-id="d7a21-119">passthru</span></span>

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

### <span data-ttu-id="d7a21-120">-ProductId</span><span class="sxs-lookup"><span data-stu-id="d7a21-120">-ProductId</span></span>
<span data-ttu-id="d7a21-121">Określa identyfikator produktu.</span><span class="sxs-lookup"><span data-stu-id="d7a21-121">Specifies the product ID.</span></span>
<span data-ttu-id="d7a21-122">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="d7a21-122">This parameter is required.</span></span>

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

### <span data-ttu-id="d7a21-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7a21-123">-DefaultProfile</span></span>
<span data-ttu-id="d7a21-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d7a21-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7a21-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7a21-125">CommonParameters</span></span>
<span data-ttu-id="d7a21-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7a21-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7a21-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7a21-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7a21-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d7a21-128">INPUTS</span></span>

## <span data-ttu-id="d7a21-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d7a21-129">OUTPUTS</span></span>

### <span data-ttu-id="d7a21-130">Wartość</span><span class="sxs-lookup"><span data-stu-id="d7a21-130">Boolean</span></span>

## <span data-ttu-id="d7a21-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d7a21-131">NOTES</span></span>

## <span data-ttu-id="d7a21-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d7a21-132">RELATED LINKS</span></span>

[<span data-ttu-id="d7a21-133">Remove-AzureRmApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="d7a21-133">Remove-AzureRmApiManagementProductFromGroup</span></span>](./Remove-AzureRmApiManagementProductFromGroup.md)


