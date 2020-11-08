---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 8C014335-9622-4F2E-A163-4B0C84531506
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementusertogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementUserToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementUserToGroup.md
ms.openlocfilehash: 27e6be451d6141e322c47b2a84a28baf115839ef
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052910"
---
# <span data-ttu-id="1e67f-101">Add-AzApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="1e67f-101">Add-AzApiManagementUserToGroup</span></span>

## <span data-ttu-id="1e67f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1e67f-102">SYNOPSIS</span></span>
<span data-ttu-id="1e67f-103">Dodaje użytkownika do grupy.</span><span class="sxs-lookup"><span data-stu-id="1e67f-103">Adds a user to a group.</span></span>

## <span data-ttu-id="1e67f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1e67f-104">SYNTAX</span></span>

```
Add-AzApiManagementUserToGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e67f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1e67f-105">DESCRIPTION</span></span>
<span data-ttu-id="1e67f-106">Polecenie cmdlet **Add-AzApiManagementUserToGroup** umożliwia dodanie użytkownika do grupy.</span><span class="sxs-lookup"><span data-stu-id="1e67f-106">The **Add-AzApiManagementUserToGroup** cmdlet adds a user to a group.</span></span>

## <span data-ttu-id="1e67f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1e67f-107">EXAMPLES</span></span>

### <span data-ttu-id="1e67f-108">Przykład 1. Dodawanie użytkownika do grupy</span><span class="sxs-lookup"><span data-stu-id="1e67f-108">Example 1: Add a user to a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementUserToGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="1e67f-109">To polecenie umożliwia dodanie istniejącego użytkownika do istniejącej grupy.</span><span class="sxs-lookup"><span data-stu-id="1e67f-109">This command adds an existing user to an existing group.</span></span>

## <span data-ttu-id="1e67f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1e67f-110">PARAMETERS</span></span>

### <span data-ttu-id="1e67f-111">-Context</span><span class="sxs-lookup"><span data-stu-id="1e67f-111">-Context</span></span>
<span data-ttu-id="1e67f-112">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="1e67f-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="1e67f-113">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="1e67f-113">This parameter is required.</span></span>

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

### <span data-ttu-id="1e67f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e67f-114">-DefaultProfile</span></span>
<span data-ttu-id="1e67f-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1e67f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e67f-116">-GroupId</span><span class="sxs-lookup"><span data-stu-id="1e67f-116">-GroupId</span></span>
<span data-ttu-id="1e67f-117">Określa identyfikator grupy.</span><span class="sxs-lookup"><span data-stu-id="1e67f-117">Specifies the group ID.</span></span>
<span data-ttu-id="1e67f-118">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="1e67f-118">This parameter is required.</span></span>

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

### <span data-ttu-id="1e67f-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1e67f-119">-PassThru</span></span>
<span data-ttu-id="1e67f-120">passthru</span><span class="sxs-lookup"><span data-stu-id="1e67f-120">passthru</span></span>

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

### <span data-ttu-id="1e67f-121">-UserId</span><span class="sxs-lookup"><span data-stu-id="1e67f-121">-UserId</span></span>
<span data-ttu-id="1e67f-122">Określa identyfikator użytkownika.</span><span class="sxs-lookup"><span data-stu-id="1e67f-122">Specifies the user ID.</span></span>
<span data-ttu-id="1e67f-123">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="1e67f-123">This parameter is required.</span></span>

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

### <span data-ttu-id="1e67f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e67f-124">CommonParameters</span></span>
<span data-ttu-id="1e67f-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e67f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e67f-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1e67f-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e67f-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1e67f-127">INPUTS</span></span>

### <span data-ttu-id="1e67f-128">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1e67f-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1e67f-129">System. String</span><span class="sxs-lookup"><span data-stu-id="1e67f-129">System.String</span></span>

### <span data-ttu-id="1e67f-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1e67f-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1e67f-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1e67f-131">OUTPUTS</span></span>

### <span data-ttu-id="1e67f-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1e67f-132">System.Boolean</span></span>

## <span data-ttu-id="1e67f-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1e67f-133">NOTES</span></span>

## <span data-ttu-id="1e67f-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1e67f-134">RELATED LINKS</span></span>

[<span data-ttu-id="1e67f-135">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="1e67f-135">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="1e67f-136">Remove-AzApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="1e67f-136">Remove-AzApiManagementUserFromGroup</span></span>](./Remove-AzApiManagementUserFromGroup.md)


