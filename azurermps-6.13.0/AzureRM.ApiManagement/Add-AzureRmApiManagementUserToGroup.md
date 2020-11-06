---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 8C014335-9622-4F2E-A163-4B0C84531506
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/add-azurermapimanagementusertogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementUserToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementUserToGroup.md
ms.openlocfilehash: abb86f40c9ac4a2ca04e0f14500df6c39e550dc3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550416"
---
# <span data-ttu-id="47992-101">Add-AzureRmApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="47992-101">Add-AzureRmApiManagementUserToGroup</span></span>

## <span data-ttu-id="47992-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="47992-102">SYNOPSIS</span></span>
<span data-ttu-id="47992-103">Dodaje użytkownika do grupy.</span><span class="sxs-lookup"><span data-stu-id="47992-103">Adds a user to a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47992-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="47992-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementUserToGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47992-105">Opis</span><span class="sxs-lookup"><span data-stu-id="47992-105">DESCRIPTION</span></span>
<span data-ttu-id="47992-106">Polecenie cmdlet **Add-AzureRmApiManagementUserToGroup** umożliwia dodanie użytkownika do grupy.</span><span class="sxs-lookup"><span data-stu-id="47992-106">The **Add-AzureRmApiManagementUserToGroup** cmdlet adds a user to a group.</span></span>

## <span data-ttu-id="47992-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="47992-107">EXAMPLES</span></span>

### <span data-ttu-id="47992-108">Przykład 1. Dodawanie użytkownika do grupy</span><span class="sxs-lookup"><span data-stu-id="47992-108">Example 1: Add a user to a group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzureRmApiManagementUserToGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="47992-109">To polecenie umożliwia dodanie istniejącego użytkownika do istniejącej grupy.</span><span class="sxs-lookup"><span data-stu-id="47992-109">This command adds an existing user to an existing group.</span></span>

## <span data-ttu-id="47992-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="47992-110">PARAMETERS</span></span>

### <span data-ttu-id="47992-111">-Context</span><span class="sxs-lookup"><span data-stu-id="47992-111">-Context</span></span>
<span data-ttu-id="47992-112">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="47992-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="47992-113">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="47992-113">This parameter is required.</span></span>

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

### <span data-ttu-id="47992-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47992-114">-DefaultProfile</span></span>
<span data-ttu-id="47992-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="47992-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47992-116">-GroupId</span><span class="sxs-lookup"><span data-stu-id="47992-116">-GroupId</span></span>
<span data-ttu-id="47992-117">Określa identyfikator grupy.</span><span class="sxs-lookup"><span data-stu-id="47992-117">Specifies the group ID.</span></span>
<span data-ttu-id="47992-118">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="47992-118">This parameter is required.</span></span>

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

### <span data-ttu-id="47992-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="47992-119">-PassThru</span></span>
<span data-ttu-id="47992-120">passthru</span><span class="sxs-lookup"><span data-stu-id="47992-120">passthru</span></span>

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

### <span data-ttu-id="47992-121">-UserId</span><span class="sxs-lookup"><span data-stu-id="47992-121">-UserId</span></span>
<span data-ttu-id="47992-122">Określa identyfikator użytkownika.</span><span class="sxs-lookup"><span data-stu-id="47992-122">Specifies the user ID.</span></span>
<span data-ttu-id="47992-123">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="47992-123">This parameter is required.</span></span>

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

### <span data-ttu-id="47992-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47992-124">CommonParameters</span></span>
<span data-ttu-id="47992-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47992-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47992-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47992-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47992-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="47992-127">INPUTS</span></span>

### <span data-ttu-id="47992-128">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="47992-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="47992-129">System. String</span><span class="sxs-lookup"><span data-stu-id="47992-129">System.String</span></span>

### <span data-ttu-id="47992-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="47992-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="47992-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="47992-131">OUTPUTS</span></span>

### <span data-ttu-id="47992-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="47992-132">System.Boolean</span></span>

## <span data-ttu-id="47992-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="47992-133">NOTES</span></span>

## <span data-ttu-id="47992-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="47992-134">RELATED LINKS</span></span>

[<span data-ttu-id="47992-135">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="47992-135">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="47992-136">Remove-AzureRmApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="47992-136">Remove-AzureRmApiManagementUserFromGroup</span></span>](./Remove-AzureRmApiManagementUserFromGroup.md)


