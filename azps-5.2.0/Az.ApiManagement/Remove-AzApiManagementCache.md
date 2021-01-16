---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCache.md
ms.openlocfilehash: ffca6c1bc32d809f7bbb93c3b76dd9490f9fafb8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362089"
---
# <span data-ttu-id="c9731-101">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="c9731-101">Remove-AzApiManagementCache</span></span>

## <span data-ttu-id="c9731-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c9731-102">SYNOPSIS</span></span>
<span data-ttu-id="c9731-103">Usuwa jednostkę pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="c9731-103">Removes the cache entity.</span></span>

## <span data-ttu-id="c9731-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c9731-104">SYNTAX</span></span>

### <span data-ttu-id="c9731-105">ContextParameterSetName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c9731-105">ContextParameterSetName (Default)</span></span>
```
Remove-AzApiManagementCache -Context <PsApiManagementContext> -CacheId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9731-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9731-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementCache -InputObject <PsApiManagementCache> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9731-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9731-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementCache -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9731-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c9731-108">DESCRIPTION</span></span>
<span data-ttu-id="c9731-109">Polecenie cmdlet **Remove-AzApiManagementCache** usuwa jednostkę pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="c9731-109">The cmdlet **Remove-AzApiManagementCache** removes the cache entity.</span></span>

## <span data-ttu-id="c9731-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c9731-110">EXAMPLES</span></span>

### <span data-ttu-id="c9731-111">Przykład 1: Usunięcie jednostki pamięci podręcznej</span><span class="sxs-lookup"><span data-stu-id="c9731-111">Example 1 : Remove the Cache entity</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementCache -Context $apimContext -CacheId "centralus"
```

<span data-ttu-id="c9731-112">To polecenie cmdlet usuwa pamięć podręczną `centralus` z usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="c9731-112">This cmdlet remove the cache `centralus` from Api Management service.</span></span>

## <span data-ttu-id="c9731-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c9731-113">PARAMETERS</span></span>

### <span data-ttu-id="c9731-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="c9731-114">-CacheId</span></span>
<span data-ttu-id="c9731-115">Identyfikator istniejącej cacheId.</span><span class="sxs-lookup"><span data-stu-id="c9731-115">Identifier of existing cacheId.</span></span>
<span data-ttu-id="c9731-116">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="c9731-116">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9731-117">-Context</span><span class="sxs-lookup"><span data-stu-id="c9731-117">-Context</span></span>
<span data-ttu-id="c9731-118">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="c9731-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="c9731-119">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="c9731-119">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9731-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9731-120">-DefaultProfile</span></span>
<span data-ttu-id="c9731-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c9731-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9731-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c9731-122">-InputObject</span></span>
<span data-ttu-id="c9731-123">Wystąpienie PsApiManagementCache.</span><span class="sxs-lookup"><span data-stu-id="c9731-123">Instance of PsApiManagementCache.</span></span> <span data-ttu-id="c9731-124">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="c9731-124">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9731-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c9731-125">-PassThru</span></span>
<span data-ttu-id="c9731-126">Jeśli ta wartość zostanie określona, operacja ta zostanie zapisana jako prawda w przypadku powodzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="c9731-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="c9731-127">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="c9731-127">This parameter is optional.</span></span>
<span data-ttu-id="c9731-128">Wartość domyślna to false.</span><span class="sxs-lookup"><span data-stu-id="c9731-128">Default value is false.</span></span>

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

### <span data-ttu-id="c9731-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c9731-129">-ResourceId</span></span>
<span data-ttu-id="c9731-130">Identyfikator zasobu ARM w pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="c9731-130">Arm ResourceId of Cache.</span></span> <span data-ttu-id="c9731-131">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="c9731-131">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9731-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c9731-132">-Confirm</span></span>
<span data-ttu-id="c9731-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9731-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9731-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9731-134">-WhatIf</span></span>
<span data-ttu-id="c9731-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9731-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9731-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c9731-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9731-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9731-137">CommonParameters</span></span>
<span data-ttu-id="c9731-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9731-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9731-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c9731-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9731-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c9731-140">INPUTS</span></span>

### <span data-ttu-id="c9731-141">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c9731-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c9731-142">System. String</span><span class="sxs-lookup"><span data-stu-id="c9731-142">System.String</span></span>

### <span data-ttu-id="c9731-143">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c9731-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c9731-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c9731-144">OUTPUTS</span></span>

### <span data-ttu-id="c9731-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c9731-145">System.Boolean</span></span>

## <span data-ttu-id="c9731-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c9731-146">NOTES</span></span>

## <span data-ttu-id="c9731-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c9731-147">RELATED LINKS</span></span>

[<span data-ttu-id="c9731-148">Nowe — AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="c9731-148">New-AzApiManagementCache</span></span>](./New-AzApiManagementCache.md)

[<span data-ttu-id="c9731-149">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="c9731-149">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)

[<span data-ttu-id="c9731-150">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="c9731-150">Update-AzApiManagementCache</span></span>](./Update-AzApiManagementCache.md)
