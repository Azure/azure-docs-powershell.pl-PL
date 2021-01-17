---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F23D9274-63B9-4654-897B-6E84757774D2
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApi.md
ms.openlocfilehash: 13f5297efc19aa56cc5af55962c072f5ff2a32d0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98342157"
---
# <span data-ttu-id="ae43d-101">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="ae43d-101">Remove-AzApiManagementApi</span></span>

## <span data-ttu-id="ae43d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ae43d-102">SYNOPSIS</span></span>
<span data-ttu-id="ae43d-103">Usuwa interfejs API.</span><span class="sxs-lookup"><span data-stu-id="ae43d-103">Removes an API.</span></span>

## <span data-ttu-id="ae43d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ae43d-104">SYNTAX</span></span>

```
Remove-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae43d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ae43d-105">DESCRIPTION</span></span>
<span data-ttu-id="ae43d-106">Polecenie cmdlet **Remove-AzApiManagementApi** usuwa istniejący interfejs API.</span><span class="sxs-lookup"><span data-stu-id="ae43d-106">The **Remove-AzApiManagementApi** cmdlet removes an existing API.</span></span>

## <span data-ttu-id="ae43d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ae43d-107">EXAMPLES</span></span>

### <span data-ttu-id="ae43d-108">Przykład 1: Usuwanie interfejsu API</span><span class="sxs-lookup"><span data-stu-id="ae43d-108">Example 1: Remove an API</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApi -Context $apimContext -ApiId "0123456789"
```

<span data-ttu-id="ae43d-109">To polecenie usuwa interfejs API o określonym IDENTYFIKATORze.</span><span class="sxs-lookup"><span data-stu-id="ae43d-109">This command removes the API with the specified ID.</span></span>

## <span data-ttu-id="ae43d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ae43d-110">PARAMETERS</span></span>

### <span data-ttu-id="ae43d-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="ae43d-111">-ApiId</span></span>
<span data-ttu-id="ae43d-112">Określa identyfikator interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="ae43d-112">Specifies the ID of the API remove.</span></span>

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

### <span data-ttu-id="ae43d-113">-Context</span><span class="sxs-lookup"><span data-stu-id="ae43d-113">-Context</span></span>
<span data-ttu-id="ae43d-114">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="ae43d-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="ae43d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae43d-115">-DefaultProfile</span></span>
<span data-ttu-id="ae43d-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ae43d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae43d-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ae43d-117">-PassThru</span></span>
<span data-ttu-id="ae43d-118">passthru</span><span class="sxs-lookup"><span data-stu-id="ae43d-118">passthru</span></span>

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

### <span data-ttu-id="ae43d-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ae43d-119">-Confirm</span></span>
<span data-ttu-id="ae43d-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae43d-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae43d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae43d-121">-WhatIf</span></span>
<span data-ttu-id="ae43d-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae43d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae43d-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ae43d-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae43d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae43d-124">CommonParameters</span></span>
<span data-ttu-id="ae43d-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae43d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae43d-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ae43d-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae43d-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ae43d-127">INPUTS</span></span>

### <span data-ttu-id="ae43d-128">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ae43d-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ae43d-129">System. String</span><span class="sxs-lookup"><span data-stu-id="ae43d-129">System.String</span></span>

### <span data-ttu-id="ae43d-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ae43d-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ae43d-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ae43d-131">OUTPUTS</span></span>

### <span data-ttu-id="ae43d-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ae43d-132">System.Boolean</span></span>

## <span data-ttu-id="ae43d-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ae43d-133">NOTES</span></span>

## <span data-ttu-id="ae43d-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ae43d-134">RELATED LINKS</span></span>

[<span data-ttu-id="ae43d-135">Eksportowanie — AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="ae43d-135">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="ae43d-136">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="ae43d-136">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="ae43d-137">Import — AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="ae43d-137">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="ae43d-138">Nowe — AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="ae43d-138">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="ae43d-139">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="ae43d-139">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


