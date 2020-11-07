---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 8C014335-9622-4F2E-A163-4B0C84531506
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/add-azurermapimanagementusertogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementUserToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementUserToGroup.md
ms.openlocfilehash: 300c99926ae7f58a6bf53ba49f3b5b86f243e150
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718064"
---
# <span data-ttu-id="2df8c-101">Add-AzureRmApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="2df8c-101">Add-AzureRmApiManagementUserToGroup</span></span>

## <span data-ttu-id="2df8c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2df8c-102">SYNOPSIS</span></span>
<span data-ttu-id="2df8c-103">Dodaje użytkownika do grupy.</span><span class="sxs-lookup"><span data-stu-id="2df8c-103">Adds a user to a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2df8c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2df8c-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementUserToGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2df8c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2df8c-105">DESCRIPTION</span></span>
<span data-ttu-id="2df8c-106">Polecenie cmdlet **Add-AzureRmApiManagementUserToGroup** umożliwia dodanie użytkownika do grupy.</span><span class="sxs-lookup"><span data-stu-id="2df8c-106">The **Add-AzureRmApiManagementUserToGroup** cmdlet adds a user to a group.</span></span>

## <span data-ttu-id="2df8c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2df8c-107">EXAMPLES</span></span>

### <span data-ttu-id="2df8c-108">Przykład 1. Dodawanie użytkownika do grupy</span><span class="sxs-lookup"><span data-stu-id="2df8c-108">Example 1: Add a user to a group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzureRmApiManagementUserToGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="2df8c-109">To polecenie umożliwia dodanie istniejącego użytkownika do istniejącej grupy.</span><span class="sxs-lookup"><span data-stu-id="2df8c-109">This command adds an existing user to an existing group.</span></span>

## <span data-ttu-id="2df8c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2df8c-110">PARAMETERS</span></span>

### <span data-ttu-id="2df8c-111">-Context</span><span class="sxs-lookup"><span data-stu-id="2df8c-111">-Context</span></span>
<span data-ttu-id="2df8c-112">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="2df8c-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="2df8c-113">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="2df8c-113">This parameter is required.</span></span>

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

### <span data-ttu-id="2df8c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2df8c-114">-DefaultProfile</span></span>
<span data-ttu-id="2df8c-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2df8c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="2df8c-116">-GroupId</span><span class="sxs-lookup"><span data-stu-id="2df8c-116">-GroupId</span></span>
<span data-ttu-id="2df8c-117">Określa identyfikator grupy.</span><span class="sxs-lookup"><span data-stu-id="2df8c-117">Specifies the group ID.</span></span>
<span data-ttu-id="2df8c-118">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="2df8c-118">This parameter is required.</span></span>

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

### <span data-ttu-id="2df8c-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2df8c-119">-PassThru</span></span>
<span data-ttu-id="2df8c-120">passthru</span><span class="sxs-lookup"><span data-stu-id="2df8c-120">passthru</span></span>

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

### <span data-ttu-id="2df8c-121">-UserId</span><span class="sxs-lookup"><span data-stu-id="2df8c-121">-UserId</span></span>
<span data-ttu-id="2df8c-122">Określa identyfikator użytkownika.</span><span class="sxs-lookup"><span data-stu-id="2df8c-122">Specifies the user ID.</span></span>
<span data-ttu-id="2df8c-123">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="2df8c-123">This parameter is required.</span></span>

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

### <span data-ttu-id="2df8c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2df8c-124">CommonParameters</span></span>
<span data-ttu-id="2df8c-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2df8c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2df8c-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2df8c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2df8c-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2df8c-127">INPUTS</span></span>

### <span data-ttu-id="2df8c-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="2df8c-128">None</span></span>
<span data-ttu-id="2df8c-129">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="2df8c-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2df8c-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2df8c-130">OUTPUTS</span></span>

### <span data-ttu-id="2df8c-131">Wartość</span><span class="sxs-lookup"><span data-stu-id="2df8c-131">Boolean</span></span>

## <span data-ttu-id="2df8c-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2df8c-132">NOTES</span></span>

## <span data-ttu-id="2df8c-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2df8c-133">RELATED LINKS</span></span>

[<span data-ttu-id="2df8c-134">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="2df8c-134">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="2df8c-135">Remove-AzureRmApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="2df8c-135">Remove-AzureRmApiManagementUserFromGroup</span></span>](./Remove-AzureRmApiManagementUserFromGroup.md)


