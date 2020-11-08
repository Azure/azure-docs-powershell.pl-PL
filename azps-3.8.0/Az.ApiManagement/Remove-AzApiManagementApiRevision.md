---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRevision.md
ms.openlocfilehash: 32677a5b8c3383b23b6ebb9832842f410a74532f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051867"
---
# <span data-ttu-id="b4424-101">Remove-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="b4424-101">Remove-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="b4424-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b4424-102">SYNOPSIS</span></span>
<span data-ttu-id="b4424-103">Usunięto określoną poprawkę interfejsu API</span><span class="sxs-lookup"><span data-stu-id="b4424-103">Removed a particular API Revision</span></span>

## <span data-ttu-id="b4424-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b4424-104">SYNTAX</span></span>

### <span data-ttu-id="b4424-105">ByApiId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b4424-105">ByApiId (Default)</span></span>
```
Remove-AzApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4424-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b4424-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiRevision -InputObject <PsApiManagementApi> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4424-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b4424-107">DESCRIPTION</span></span>
<span data-ttu-id="b4424-108">Polecenie cmdlet **Remove-AzApiManagementApiRevision** usuwa określoną poprawkę interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="b4424-108">The cmdlet **Remove-AzApiManagementApiRevision** removes a particular API revision.</span></span>

## <span data-ttu-id="b4424-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b4424-109">EXAMPLES</span></span>

### <span data-ttu-id="b4424-110">Przykład 1: usuwanie poprawki interfejsu API</span><span class="sxs-lookup"><span data-stu-id="b4424-110">Example 1: Remove an API Revision</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzAzureRmApiManagementApiRevision -Context $apimContext -ApiId "echo-api" -ApiRevision "2"
```

<span data-ttu-id="b4424-111">To polecenie usuwa `2` wersję interfejsu API `echo-api` z usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="b4424-111">This command removes the `2` revision of the API `echo-api` from API Management service.</span></span>

## <span data-ttu-id="b4424-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b4424-112">PARAMETERS</span></span>

### <span data-ttu-id="b4424-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="b4424-113">-ApiId</span></span>
<span data-ttu-id="b4424-114">Identyfikator interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="b4424-114">Identifier of the API.</span></span>
<span data-ttu-id="b4424-115">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="b4424-115">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4424-116">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="b4424-116">-ApiRevision</span></span>
<span data-ttu-id="b4424-117">Identyfikator poprawki interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="b4424-117">Identifier of the API Revision.</span></span> <span data-ttu-id="b4424-118">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="b4424-118">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4424-119">-Context</span><span class="sxs-lookup"><span data-stu-id="b4424-119">-Context</span></span>
<span data-ttu-id="b4424-120">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="b4424-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b4424-121">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="b4424-121">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ByApiId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4424-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4424-122">-DefaultProfile</span></span>
<span data-ttu-id="b4424-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b4424-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4424-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b4424-124">-InputObject</span></span>
<span data-ttu-id="b4424-125">Wystąpienie PsApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="b4424-125">Instance of PsApiManagementApiRelease.</span></span> <span data-ttu-id="b4424-126">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="b4424-126">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4424-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b4424-127">-PassThru</span></span>
<span data-ttu-id="b4424-128">Jeśli ta wartość zostanie określona, operacja ta zostanie zapisana jako prawda w przypadku powodzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="b4424-128">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="b4424-129">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="b4424-129">This parameter is optional.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4424-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b4424-130">-Confirm</span></span>
<span data-ttu-id="b4424-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4424-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4424-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4424-132">-WhatIf</span></span>
<span data-ttu-id="b4424-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4424-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4424-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b4424-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4424-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4424-135">CommonParameters</span></span>
<span data-ttu-id="b4424-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4424-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4424-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b4424-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4424-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b4424-138">INPUTS</span></span>

### <span data-ttu-id="b4424-139">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b4424-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b4424-140">System. String</span><span class="sxs-lookup"><span data-stu-id="b4424-140">System.String</span></span>

### <span data-ttu-id="b4424-141">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="b4424-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="b4424-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b4424-142">OUTPUTS</span></span>

### <span data-ttu-id="b4424-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b4424-143">System.Boolean</span></span>

## <span data-ttu-id="b4424-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b4424-144">NOTES</span></span>

## <span data-ttu-id="b4424-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b4424-145">RELATED LINKS</span></span>

[<span data-ttu-id="b4424-146">Get-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="b4424-146">Get-AzApiManagementApiRevision</span></span>](./Get-AzApiManagementApiRevision.md)

[<span data-ttu-id="b4424-147">Nowe — AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="b4424-147">New-AzApiManagementApiRevision</span></span>](./New-AzApiManagementApiRevision.md)

[<span data-ttu-id="b4424-148">Set-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="b4424-148">Set-AzApiManagementApiRevision</span></span>](./Set-AzApiManagementApiRevision.md)