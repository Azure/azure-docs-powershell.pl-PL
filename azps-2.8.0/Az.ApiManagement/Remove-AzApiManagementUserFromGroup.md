---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F0BDB0EE-1F26-450D-9C68-34C79CE8F778
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementuserfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUserFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUserFromGroup.md
ms.openlocfilehash: 73d21a78fd71a677c03e52e131abb7050d71fffc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706929"
---
# <span data-ttu-id="79851-101">Remove-AzApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="79851-101">Remove-AzApiManagementUserFromGroup</span></span>

## <span data-ttu-id="79851-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="79851-102">SYNOPSIS</span></span>
<span data-ttu-id="79851-103">Usuwa użytkownika z grupy.</span><span class="sxs-lookup"><span data-stu-id="79851-103">Removes a user from a group.</span></span>

## <span data-ttu-id="79851-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="79851-104">SYNTAX</span></span>

```
Remove-AzApiManagementUserFromGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79851-105">Opis</span><span class="sxs-lookup"><span data-stu-id="79851-105">DESCRIPTION</span></span>
<span data-ttu-id="79851-106">Polecenie cmdlet **Remove-AzApiManagementUserFromGroup** usuwa użytkownika z istniejącej grupy.</span><span class="sxs-lookup"><span data-stu-id="79851-106">The **Remove-AzApiManagementUserFromGroup** cmdlet removes a user from an existing group.</span></span>

## <span data-ttu-id="79851-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="79851-107">EXAMPLES</span></span>

### <span data-ttu-id="79851-108">Przykład 1: Usuwanie użytkownika z grupy</span><span class="sxs-lookup"><span data-stu-id="79851-108">Example 1: Remove a user from a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementUserFromGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="79851-109">To polecenie umożliwia usunięcie użytkownika z grupy.</span><span class="sxs-lookup"><span data-stu-id="79851-109">This command removes a user from a group.</span></span>

## <span data-ttu-id="79851-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="79851-110">PARAMETERS</span></span>

### <span data-ttu-id="79851-111">-Context</span><span class="sxs-lookup"><span data-stu-id="79851-111">-Context</span></span>
<span data-ttu-id="79851-112">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="79851-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="79851-113">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="79851-113">This parameter is required.</span></span>

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

### <span data-ttu-id="79851-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79851-114">-DefaultProfile</span></span>
<span data-ttu-id="79851-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="79851-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79851-116">-GroupId</span><span class="sxs-lookup"><span data-stu-id="79851-116">-GroupId</span></span>
<span data-ttu-id="79851-117">Określa identyfikator grupy, z której należy usunąć użytkownika.</span><span class="sxs-lookup"><span data-stu-id="79851-117">Specifies the ID of the group from which to remove a user.</span></span>

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

### <span data-ttu-id="79851-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="79851-118">-PassThru</span></span>
<span data-ttu-id="79851-119">Wskazuje, że to polecenie cmdlet zwraca wartość $True, jeśli się powiodło, lub wartość $False w przeciwnym razie.</span><span class="sxs-lookup"><span data-stu-id="79851-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="79851-120">-UserId</span><span class="sxs-lookup"><span data-stu-id="79851-120">-UserId</span></span>
<span data-ttu-id="79851-121">Określa identyfikator użytkownika, który ma zostać usunięty z grupy.</span><span class="sxs-lookup"><span data-stu-id="79851-121">Specifies the ID of the user to remove from the group.</span></span>

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

### <span data-ttu-id="79851-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79851-122">CommonParameters</span></span>
<span data-ttu-id="79851-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79851-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79851-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="79851-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79851-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="79851-125">INPUTS</span></span>

### <span data-ttu-id="79851-126">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="79851-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="79851-127">System. String</span><span class="sxs-lookup"><span data-stu-id="79851-127">System.String</span></span>

### <span data-ttu-id="79851-128">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="79851-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="79851-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="79851-129">OUTPUTS</span></span>

### <span data-ttu-id="79851-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="79851-130">System.Boolean</span></span>

## <span data-ttu-id="79851-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="79851-131">NOTES</span></span>

## <span data-ttu-id="79851-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="79851-132">RELATED LINKS</span></span>

[<span data-ttu-id="79851-133">Dodaj-AzApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="79851-133">Add-AzApiManagementUserToGroup</span></span>](./Add-AzApiManagementUserToGroup.md)

[<span data-ttu-id="79851-134">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="79851-134">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)


