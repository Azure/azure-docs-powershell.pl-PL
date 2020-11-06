---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiRevision.md
ms.openlocfilehash: cd32f29a0202fa8c38abed43075a8623efe068a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524722"
---
# <span data-ttu-id="8bcba-101">Remove-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="8bcba-101">Remove-AzureRmApiManagementApiRevision</span></span>

## <span data-ttu-id="8bcba-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8bcba-102">SYNOPSIS</span></span>
<span data-ttu-id="8bcba-103">Usunięto określoną poprawkę interfejsu API</span><span class="sxs-lookup"><span data-stu-id="8bcba-103">Removed a particular API Revision</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8bcba-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8bcba-104">SYNTAX</span></span>

### <span data-ttu-id="8bcba-105">ByApiId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8bcba-105">ByApiId (Default)</span></span>
```
Remove-AzureRmApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8bcba-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8bcba-106">ByInputObject</span></span>
```
Remove-AzureRmApiManagementApiRevision -InputObject <PsApiManagementApi> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8bcba-107">Opis</span><span class="sxs-lookup"><span data-stu-id="8bcba-107">DESCRIPTION</span></span>
<span data-ttu-id="8bcba-108">Polecenie cmdlet **Remove-AzureRmApiManagementApiRevision** usuwa określoną poprawkę interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="8bcba-108">The cmdlet **Remove-AzureRmApiManagementApiRevision** removes a particular API revision.</span></span>

## <span data-ttu-id="8bcba-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8bcba-109">EXAMPLES</span></span>

### <span data-ttu-id="8bcba-110">Przykład 1: usuwanie poprawki interfejsu API</span><span class="sxs-lookup"><span data-stu-id="8bcba-110">Example 1: Remove an API Revision</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementApiRevision -Context $apimContext -ApiId "echo-api" -ApiRevision "2"
```

<span data-ttu-id="8bcba-111">To polecenie usuwa `2` wersję interfejsu API `echo-api` z usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="8bcba-111">This command removes the `2` revision of the API `echo-api` from API Management service.</span></span>

## <span data-ttu-id="8bcba-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8bcba-112">PARAMETERS</span></span>

### <span data-ttu-id="8bcba-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="8bcba-113">-ApiId</span></span>
<span data-ttu-id="8bcba-114">Identyfikator interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="8bcba-114">Identifier of the API.</span></span>
<span data-ttu-id="8bcba-115">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="8bcba-115">This parameter is required.</span></span>

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

### <span data-ttu-id="8bcba-116">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="8bcba-116">-ApiRevision</span></span>
<span data-ttu-id="8bcba-117">Identyfikator poprawki interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="8bcba-117">Identifier of the API Revision.</span></span> <span data-ttu-id="8bcba-118">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="8bcba-118">This parameter is required.</span></span>

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

### <span data-ttu-id="8bcba-119">-Context</span><span class="sxs-lookup"><span data-stu-id="8bcba-119">-Context</span></span>
<span data-ttu-id="8bcba-120">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="8bcba-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="8bcba-121">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="8bcba-121">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ByApiId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bcba-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bcba-122">-DefaultProfile</span></span>
<span data-ttu-id="8bcba-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8bcba-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8bcba-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8bcba-124">-InputObject</span></span>
<span data-ttu-id="8bcba-125">Wystąpienie PsApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="8bcba-125">Instance of PsApiManagementApiRelease.</span></span> <span data-ttu-id="8bcba-126">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="8bcba-126">This parameter is required.</span></span>

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

### <span data-ttu-id="8bcba-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8bcba-127">-PassThru</span></span>
<span data-ttu-id="8bcba-128">Jeśli ta wartość zostanie określona, operacja ta zostanie zapisana jako prawda w przypadku powodzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="8bcba-128">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="8bcba-129">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="8bcba-129">This parameter is optional.</span></span>

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

### <span data-ttu-id="8bcba-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8bcba-130">-Confirm</span></span>
<span data-ttu-id="8bcba-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8bcba-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8bcba-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bcba-132">-WhatIf</span></span>
<span data-ttu-id="8bcba-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8bcba-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8bcba-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8bcba-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8bcba-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bcba-135">CommonParameters</span></span>
<span data-ttu-id="8bcba-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bcba-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bcba-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bcba-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bcba-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8bcba-138">INPUTS</span></span>

### <span data-ttu-id="8bcba-139">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8bcba-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8bcba-140">System. String</span><span class="sxs-lookup"><span data-stu-id="8bcba-140">System.String</span></span>

### <span data-ttu-id="8bcba-141">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="8bcba-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>
<span data-ttu-id="8bcba-142">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8bcba-142">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="8bcba-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8bcba-143">OUTPUTS</span></span>

### <span data-ttu-id="8bcba-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8bcba-144">System.Boolean</span></span>

## <span data-ttu-id="8bcba-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8bcba-145">NOTES</span></span>

## <span data-ttu-id="8bcba-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8bcba-146">RELATED LINKS</span></span>

[<span data-ttu-id="8bcba-147">Get-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="8bcba-147">Get-AzureRmApiManagementApiRevision</span></span>](./Get-AzureRmApiManagementApiRevision.md)

[<span data-ttu-id="8bcba-148">Nowe — AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="8bcba-148">New-AzureRmApiManagementApiRevision</span></span>](./New-AzureRmApiManagementApiRevision.md)

[<span data-ttu-id="8bcba-149">Set-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="8bcba-149">Set-AzureRmApiManagementApiRevision</span></span>](./Set-AzureRmApiManagementApiRevision.md)
