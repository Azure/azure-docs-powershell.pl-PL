---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: F0BDB0EE-1F26-450D-9C68-34C79CE8F778
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUserFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUserFromGroup.md
ms.openlocfilehash: 2867e8eec65de040a0da61a1af960abc9797bb18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717882"
---
# <span data-ttu-id="2b1a8-101">Remove-AzureRmApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="2b1a8-101">Remove-AzureRmApiManagementUserFromGroup</span></span>

## <span data-ttu-id="2b1a8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2b1a8-102">SYNOPSIS</span></span>
<span data-ttu-id="2b1a8-103">Usuwa użytkownika z grupy.</span><span class="sxs-lookup"><span data-stu-id="2b1a8-103">Removes a user from a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b1a8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2b1a8-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementUserFromGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b1a8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2b1a8-105">DESCRIPTION</span></span>
<span data-ttu-id="2b1a8-106">Polecenie cmdlet **Remove-AzureRmApiManagementUserFromGroup** usuwa użytkownika z istniejącej grupy.</span><span class="sxs-lookup"><span data-stu-id="2b1a8-106">The **Remove-AzureRmApiManagementUserFromGroup** cmdlet removes a user from an existing group.</span></span>

## <span data-ttu-id="2b1a8-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2b1a8-107">EXAMPLES</span></span>

### <span data-ttu-id="2b1a8-108">Przykład 1: Usuwanie użytkownika z grupy</span><span class="sxs-lookup"><span data-stu-id="2b1a8-108">Example 1: Remove a user from a group</span></span>
```
PS C:\>Remove-AzureRmApiManagementUserFromGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="2b1a8-109">To polecenie umożliwia usunięcie użytkownika z grupy.</span><span class="sxs-lookup"><span data-stu-id="2b1a8-109">This command removes a user from a group.</span></span>

## <span data-ttu-id="2b1a8-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2b1a8-110">PARAMETERS</span></span>

### <span data-ttu-id="2b1a8-111">-Context</span><span class="sxs-lookup"><span data-stu-id="2b1a8-111">-Context</span></span>
<span data-ttu-id="2b1a8-112">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="2b1a8-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="2b1a8-113">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="2b1a8-113">This parameter is required.</span></span>

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

### <span data-ttu-id="2b1a8-114">-GroupId</span><span class="sxs-lookup"><span data-stu-id="2b1a8-114">-GroupId</span></span>
<span data-ttu-id="2b1a8-115">Określa identyfikator grupy, z której należy usunąć użytkownika.</span><span class="sxs-lookup"><span data-stu-id="2b1a8-115">Specifies the ID of the group from which to remove a user.</span></span>

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

### <span data-ttu-id="2b1a8-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2b1a8-116">-PassThru</span></span>
<span data-ttu-id="2b1a8-117">Wskazuje, że to polecenie cmdlet zwraca wartość $True, jeśli się powiodło, lub wartość $False w przeciwnym razie.</span><span class="sxs-lookup"><span data-stu-id="2b1a8-117">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="2b1a8-118">-UserId</span><span class="sxs-lookup"><span data-stu-id="2b1a8-118">-UserId</span></span>
<span data-ttu-id="2b1a8-119">Określa identyfikator użytkownika, który ma zostać usunięty z grupy.</span><span class="sxs-lookup"><span data-stu-id="2b1a8-119">Specifies the ID of the user to remove from the group.</span></span>

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

### <span data-ttu-id="2b1a8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b1a8-120">-DefaultProfile</span></span>
<span data-ttu-id="2b1a8-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2b1a8-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b1a8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b1a8-122">CommonParameters</span></span>
<span data-ttu-id="2b1a8-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b1a8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b1a8-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b1a8-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b1a8-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2b1a8-125">INPUTS</span></span>

## <span data-ttu-id="2b1a8-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2b1a8-126">OUTPUTS</span></span>

### <span data-ttu-id="2b1a8-127">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2b1a8-127">System.Boolean</span></span>

## <span data-ttu-id="2b1a8-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2b1a8-128">NOTES</span></span>

## <span data-ttu-id="2b1a8-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2b1a8-129">RELATED LINKS</span></span>

[<span data-ttu-id="2b1a8-130">Dodaj-AzureRmApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="2b1a8-130">Add-AzureRmApiManagementUserToGroup</span></span>](./Add-AzureRmApiManagementUserToGroup.md)

[<span data-ttu-id="2b1a8-131">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="2b1a8-131">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

