---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 8C014335-9622-4F2E-A163-4B0C84531506
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementUserToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementUserToGroup.md
ms.openlocfilehash: d405dc21719abc1aec5767f4d1b89a938b79eaf9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528362"
---
# <span data-ttu-id="6fbd4-101">Add-AzureRmApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="6fbd4-101">Add-AzureRmApiManagementUserToGroup</span></span>

## <span data-ttu-id="6fbd4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6fbd4-102">SYNOPSIS</span></span>
<span data-ttu-id="6fbd4-103">Dodaje użytkownika do grupy.</span><span class="sxs-lookup"><span data-stu-id="6fbd4-103">Adds a user to a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6fbd4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6fbd4-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementUserToGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6fbd4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6fbd4-105">DESCRIPTION</span></span>
<span data-ttu-id="6fbd4-106">Polecenie cmdlet **Add-AzureRmApiManagementUserToGroup** umożliwia dodanie użytkownika do grupy.</span><span class="sxs-lookup"><span data-stu-id="6fbd4-106">The **Add-AzureRmApiManagementUserToGroup** cmdlet adds a user to a group.</span></span>

## <span data-ttu-id="6fbd4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6fbd4-107">EXAMPLES</span></span>

### <span data-ttu-id="6fbd4-108">Przykład 1. Dodawanie użytkownika do grupy</span><span class="sxs-lookup"><span data-stu-id="6fbd4-108">Example 1: Add a user to a group</span></span>
```
PS C:\>Add-AzureRmApiManagementUserToGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="6fbd4-109">To polecenie umożliwia dodanie istniejącego użytkownika do istniejącej grupy.</span><span class="sxs-lookup"><span data-stu-id="6fbd4-109">This command adds an existing user to an existing group.</span></span>

## <span data-ttu-id="6fbd4-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6fbd4-110">PARAMETERS</span></span>

### <span data-ttu-id="6fbd4-111">-Context</span><span class="sxs-lookup"><span data-stu-id="6fbd4-111">-Context</span></span>
<span data-ttu-id="6fbd4-112">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="6fbd4-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="6fbd4-113">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="6fbd4-113">This parameter is required.</span></span>

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

### <span data-ttu-id="6fbd4-114">-GroupId</span><span class="sxs-lookup"><span data-stu-id="6fbd4-114">-GroupId</span></span>
<span data-ttu-id="6fbd4-115">Określa identyfikator grupy.</span><span class="sxs-lookup"><span data-stu-id="6fbd4-115">Specifies the group ID.</span></span>
<span data-ttu-id="6fbd4-116">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="6fbd4-116">This parameter is required.</span></span>

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

### <span data-ttu-id="6fbd4-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6fbd4-117">-PassThru</span></span>
<span data-ttu-id="6fbd4-118">passthru</span><span class="sxs-lookup"><span data-stu-id="6fbd4-118">passthru</span></span>

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

### <span data-ttu-id="6fbd4-119">-UserId</span><span class="sxs-lookup"><span data-stu-id="6fbd4-119">-UserId</span></span>
<span data-ttu-id="6fbd4-120">Określa identyfikator użytkownika.</span><span class="sxs-lookup"><span data-stu-id="6fbd4-120">Specifies the user ID.</span></span>
<span data-ttu-id="6fbd4-121">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="6fbd4-121">This parameter is required.</span></span>

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

### <span data-ttu-id="6fbd4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fbd4-122">-DefaultProfile</span></span>
<span data-ttu-id="6fbd4-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6fbd4-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6fbd4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fbd4-124">CommonParameters</span></span>
<span data-ttu-id="6fbd4-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fbd4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fbd4-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fbd4-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fbd4-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6fbd4-127">INPUTS</span></span>

## <span data-ttu-id="6fbd4-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6fbd4-128">OUTPUTS</span></span>

### <span data-ttu-id="6fbd4-129">Wartość</span><span class="sxs-lookup"><span data-stu-id="6fbd4-129">Boolean</span></span>

## <span data-ttu-id="6fbd4-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6fbd4-130">NOTES</span></span>

## <span data-ttu-id="6fbd4-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6fbd4-131">RELATED LINKS</span></span>

[<span data-ttu-id="6fbd4-132">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="6fbd4-132">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="6fbd4-133">Remove-AzureRmApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="6fbd4-133">Remove-AzureRmApiManagementUserFromGroup</span></span>](./Remove-AzureRmApiManagementUserFromGroup.md)


