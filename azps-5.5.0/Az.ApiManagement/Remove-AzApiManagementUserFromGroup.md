---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F0BDB0EE-1F26-450D-9C68-34C79CE8F778
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementuserfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUserFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUserFromGroup.md
ms.openlocfilehash: 220af172efa397de2fc0fafa7597c2b6e29dae60
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197162"
---
# <span data-ttu-id="0c7cd-101">Remove-AzApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="0c7cd-101">Remove-AzApiManagementUserFromGroup</span></span>

## <span data-ttu-id="0c7cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c7cd-102">SYNOPSIS</span></span>
<span data-ttu-id="0c7cd-103">Usuwa użytkownika z grupy.</span><span class="sxs-lookup"><span data-stu-id="0c7cd-103">Removes a user from a group.</span></span>

## <span data-ttu-id="0c7cd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0c7cd-104">SYNTAX</span></span>

```
Remove-AzApiManagementUserFromGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c7cd-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="0c7cd-105">DESCRIPTION</span></span>
<span data-ttu-id="0c7cd-106">Polecenie **cmdlet Remove-AzApiManagementUserFromGroup** usuwa użytkownika z istniejącej grupy.</span><span class="sxs-lookup"><span data-stu-id="0c7cd-106">The **Remove-AzApiManagementUserFromGroup** cmdlet removes a user from an existing group.</span></span>

## <span data-ttu-id="0c7cd-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0c7cd-107">EXAMPLES</span></span>

### <span data-ttu-id="0c7cd-108">Przykład 1. Usuwanie użytkownika z grupy</span><span class="sxs-lookup"><span data-stu-id="0c7cd-108">Example 1: Remove a user from a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementUserFromGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="0c7cd-109">To polecenie usuwa użytkownika z grupy.</span><span class="sxs-lookup"><span data-stu-id="0c7cd-109">This command removes a user from a group.</span></span>

## <span data-ttu-id="0c7cd-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0c7cd-110">PARAMETERS</span></span>

### <span data-ttu-id="0c7cd-111">— kontekst</span><span class="sxs-lookup"><span data-stu-id="0c7cd-111">-Context</span></span>
<span data-ttu-id="0c7cd-112">Określa obiekt **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="0c7cd-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="0c7cd-113">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="0c7cd-113">This parameter is required.</span></span>

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

### <span data-ttu-id="0c7cd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c7cd-114">-DefaultProfile</span></span>
<span data-ttu-id="0c7cd-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0c7cd-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c7cd-116">- GroupId</span><span class="sxs-lookup"><span data-stu-id="0c7cd-116">-GroupId</span></span>
<span data-ttu-id="0c7cd-117">Określa identyfikator grupy, z której chcesz usunąć użytkownika.</span><span class="sxs-lookup"><span data-stu-id="0c7cd-117">Specifies the ID of the group from which to remove a user.</span></span>

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

### <span data-ttu-id="0c7cd-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0c7cd-118">-PassThru</span></span>
<span data-ttu-id="0c7cd-119">Wskazuje, że to polecenie cmdlet zwraca wartość $True, jeśli się powiedzie, lub wartość $False w przeciwnym razie.</span><span class="sxs-lookup"><span data-stu-id="0c7cd-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="0c7cd-120">-UserId</span><span class="sxs-lookup"><span data-stu-id="0c7cd-120">-UserId</span></span>
<span data-ttu-id="0c7cd-121">Określa identyfikator użytkownika do usunięcia z grupy.</span><span class="sxs-lookup"><span data-stu-id="0c7cd-121">Specifies the ID of the user to remove from the group.</span></span>

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

### <span data-ttu-id="0c7cd-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c7cd-122">CommonParameters</span></span>
<span data-ttu-id="0c7cd-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c7cd-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c7cd-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0c7cd-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c7cd-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0c7cd-125">INPUTS</span></span>

### <span data-ttu-id="0c7cd-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0c7cd-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0c7cd-127">System.String</span><span class="sxs-lookup"><span data-stu-id="0c7cd-127">System.String</span></span>

### <span data-ttu-id="0c7cd-128">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="0c7cd-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0c7cd-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0c7cd-129">OUTPUTS</span></span>

### <span data-ttu-id="0c7cd-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0c7cd-130">System.Boolean</span></span>

## <span data-ttu-id="0c7cd-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0c7cd-131">NOTES</span></span>

## <span data-ttu-id="0c7cd-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0c7cd-132">RELATED LINKS</span></span>

[<span data-ttu-id="0c7cd-133">Add-AzApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="0c7cd-133">Add-AzApiManagementUserToGroup</span></span>](./Add-AzApiManagementUserToGroup.md)

[<span data-ttu-id="0c7cd-134">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="0c7cd-134">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)


