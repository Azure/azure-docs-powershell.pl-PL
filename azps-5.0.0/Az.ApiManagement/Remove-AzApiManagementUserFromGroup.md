---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F0BDB0EE-1F26-450D-9C68-34C79CE8F778
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementuserfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUserFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUserFromGroup.md
ms.openlocfilehash: 220af172efa397de2fc0fafa7597c2b6e29dae60
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232616"
---
# <span data-ttu-id="4b85b-101">Remove-AzApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="4b85b-101">Remove-AzApiManagementUserFromGroup</span></span>

## <span data-ttu-id="4b85b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4b85b-102">SYNOPSIS</span></span>
<span data-ttu-id="4b85b-103">Usuwa użytkownika z grupy.</span><span class="sxs-lookup"><span data-stu-id="4b85b-103">Removes a user from a group.</span></span>

## <span data-ttu-id="4b85b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4b85b-104">SYNTAX</span></span>

```
Remove-AzApiManagementUserFromGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b85b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4b85b-105">DESCRIPTION</span></span>
<span data-ttu-id="4b85b-106">Polecenie cmdlet **Remove-AzApiManagementUserFromGroup** usuwa użytkownika z istniejącej grupy.</span><span class="sxs-lookup"><span data-stu-id="4b85b-106">The **Remove-AzApiManagementUserFromGroup** cmdlet removes a user from an existing group.</span></span>

## <span data-ttu-id="4b85b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4b85b-107">EXAMPLES</span></span>

### <span data-ttu-id="4b85b-108">Przykład 1: Usuwanie użytkownika z grupy</span><span class="sxs-lookup"><span data-stu-id="4b85b-108">Example 1: Remove a user from a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementUserFromGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="4b85b-109">To polecenie umożliwia usunięcie użytkownika z grupy.</span><span class="sxs-lookup"><span data-stu-id="4b85b-109">This command removes a user from a group.</span></span>

## <span data-ttu-id="4b85b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4b85b-110">PARAMETERS</span></span>

### <span data-ttu-id="4b85b-111">-Context</span><span class="sxs-lookup"><span data-stu-id="4b85b-111">-Context</span></span>
<span data-ttu-id="4b85b-112">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="4b85b-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="4b85b-113">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="4b85b-113">This parameter is required.</span></span>

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

### <span data-ttu-id="4b85b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b85b-114">-DefaultProfile</span></span>
<span data-ttu-id="4b85b-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4b85b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b85b-116">-GroupId</span><span class="sxs-lookup"><span data-stu-id="4b85b-116">-GroupId</span></span>
<span data-ttu-id="4b85b-117">Określa identyfikator grupy, z której należy usunąć użytkownika.</span><span class="sxs-lookup"><span data-stu-id="4b85b-117">Specifies the ID of the group from which to remove a user.</span></span>

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

### <span data-ttu-id="4b85b-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4b85b-118">-PassThru</span></span>
<span data-ttu-id="4b85b-119">Wskazuje, że to polecenie cmdlet zwraca wartość $True, jeśli się powiodło, lub wartość $False w przeciwnym razie.</span><span class="sxs-lookup"><span data-stu-id="4b85b-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="4b85b-120">-UserId</span><span class="sxs-lookup"><span data-stu-id="4b85b-120">-UserId</span></span>
<span data-ttu-id="4b85b-121">Określa identyfikator użytkownika, który ma zostać usunięty z grupy.</span><span class="sxs-lookup"><span data-stu-id="4b85b-121">Specifies the ID of the user to remove from the group.</span></span>

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

### <span data-ttu-id="4b85b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b85b-122">CommonParameters</span></span>
<span data-ttu-id="4b85b-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b85b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b85b-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4b85b-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b85b-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4b85b-125">INPUTS</span></span>

### <span data-ttu-id="4b85b-126">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4b85b-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4b85b-127">System. String</span><span class="sxs-lookup"><span data-stu-id="4b85b-127">System.String</span></span>

### <span data-ttu-id="4b85b-128">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4b85b-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4b85b-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4b85b-129">OUTPUTS</span></span>

### <span data-ttu-id="4b85b-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4b85b-130">System.Boolean</span></span>

## <span data-ttu-id="4b85b-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4b85b-131">NOTES</span></span>

## <span data-ttu-id="4b85b-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4b85b-132">RELATED LINKS</span></span>

[<span data-ttu-id="4b85b-133">Dodaj-AzApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="4b85b-133">Add-AzApiManagementUserToGroup</span></span>](./Add-AzApiManagementUserToGroup.md)

[<span data-ttu-id="4b85b-134">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="4b85b-134">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)


