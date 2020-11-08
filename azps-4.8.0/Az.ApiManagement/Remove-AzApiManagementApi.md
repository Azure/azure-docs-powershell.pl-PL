---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F23D9274-63B9-4654-897B-6E84757774D2
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApi.md
ms.openlocfilehash: 13f5297efc19aa56cc5af55962c072f5ff2a32d0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222721"
---
# <span data-ttu-id="4494e-101">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4494e-101">Remove-AzApiManagementApi</span></span>

## <span data-ttu-id="4494e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4494e-102">SYNOPSIS</span></span>
<span data-ttu-id="4494e-103">Usuwa interfejs API.</span><span class="sxs-lookup"><span data-stu-id="4494e-103">Removes an API.</span></span>

## <span data-ttu-id="4494e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4494e-104">SYNTAX</span></span>

```
Remove-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4494e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4494e-105">DESCRIPTION</span></span>
<span data-ttu-id="4494e-106">Polecenie cmdlet **Remove-AzApiManagementApi** usuwa istniejący interfejs API.</span><span class="sxs-lookup"><span data-stu-id="4494e-106">The **Remove-AzApiManagementApi** cmdlet removes an existing API.</span></span>

## <span data-ttu-id="4494e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4494e-107">EXAMPLES</span></span>

### <span data-ttu-id="4494e-108">Przykład 1: Usuwanie interfejsu API</span><span class="sxs-lookup"><span data-stu-id="4494e-108">Example 1: Remove an API</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApi -Context $apimContext -ApiId "0123456789"
```

<span data-ttu-id="4494e-109">To polecenie usuwa interfejs API o określonym IDENTYFIKATORze.</span><span class="sxs-lookup"><span data-stu-id="4494e-109">This command removes the API with the specified ID.</span></span>

## <span data-ttu-id="4494e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4494e-110">PARAMETERS</span></span>

### <span data-ttu-id="4494e-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="4494e-111">-ApiId</span></span>
<span data-ttu-id="4494e-112">Określa identyfikator interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="4494e-112">Specifies the ID of the API remove.</span></span>

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

### <span data-ttu-id="4494e-113">-Context</span><span class="sxs-lookup"><span data-stu-id="4494e-113">-Context</span></span>
<span data-ttu-id="4494e-114">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="4494e-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="4494e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4494e-115">-DefaultProfile</span></span>
<span data-ttu-id="4494e-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4494e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4494e-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4494e-117">-PassThru</span></span>
<span data-ttu-id="4494e-118">passthru</span><span class="sxs-lookup"><span data-stu-id="4494e-118">passthru</span></span>

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

### <span data-ttu-id="4494e-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4494e-119">-Confirm</span></span>
<span data-ttu-id="4494e-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4494e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4494e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4494e-121">-WhatIf</span></span>
<span data-ttu-id="4494e-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4494e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4494e-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4494e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4494e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4494e-124">CommonParameters</span></span>
<span data-ttu-id="4494e-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4494e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4494e-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4494e-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4494e-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4494e-127">INPUTS</span></span>

### <span data-ttu-id="4494e-128">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4494e-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4494e-129">System. String</span><span class="sxs-lookup"><span data-stu-id="4494e-129">System.String</span></span>

### <span data-ttu-id="4494e-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4494e-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4494e-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4494e-131">OUTPUTS</span></span>

### <span data-ttu-id="4494e-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4494e-132">System.Boolean</span></span>

## <span data-ttu-id="4494e-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4494e-133">NOTES</span></span>

## <span data-ttu-id="4494e-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4494e-134">RELATED LINKS</span></span>

[<span data-ttu-id="4494e-135">Eksportowanie — AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4494e-135">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="4494e-136">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4494e-136">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="4494e-137">Import — AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4494e-137">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="4494e-138">Nowe — AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4494e-138">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="4494e-139">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4494e-139">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


