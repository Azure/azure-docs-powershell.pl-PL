---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C791C593-F7D5-4961-97F9-E4909813FFE7
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADApplication.md
ms.openlocfilehash: 3059e5611f843244f69cc48ae432ef070627d29d
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100407730"
---
# <span data-ttu-id="354f3-101">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="354f3-101">Remove-AzADApplication</span></span>

## <span data-ttu-id="354f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="354f3-102">SYNOPSIS</span></span>
<span data-ttu-id="354f3-103">Usuwa aplikację usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="354f3-103">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="354f3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="354f3-104">SYNTAX</span></span>

### <span data-ttu-id="354f3-105">ObjectIdParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="354f3-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADApplication -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="354f3-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="354f3-106">ApplicationIdParameterSet</span></span>
```
Remove-AzADApplication -ApplicationId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="354f3-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="354f3-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzADApplication -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="354f3-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="354f3-108">InputObjectParameterSet</span></span>
```
Remove-AzADApplication -InputObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="354f3-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="354f3-109">DESCRIPTION</span></span>
<span data-ttu-id="354f3-110">Usuwa aplikację usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="354f3-110">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="354f3-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="354f3-111">EXAMPLES</span></span>

### <span data-ttu-id="354f3-112">Przykład 1. Usuwanie aplikacji według identyfikatora obiektu</span><span class="sxs-lookup"><span data-stu-id="354f3-112">Example 1 - Remove application by object id</span></span>

```
PS C:\> Remove-AzADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738
```

<span data-ttu-id="354f3-113">Usuwa aplikację z dzierżawy o identyfikatorze obiektu "b4cd1619-80b3-4cfb-9f8f-9f2333425738".</span><span class="sxs-lookup"><span data-stu-id="354f3-113">Removes the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' from the tenant.</span></span>

### <span data-ttu-id="354f3-114">Przykład 2. Usuwanie aplikacji według identyfikatora aplikacji</span><span class="sxs-lookup"><span data-stu-id="354f3-114">Example 2 - Remove application by application id</span></span>

```
PS C:\> Remove-AzADApplication -ApplicationId f9c5ea4f-28f0-401a-a491-491a037fa346
```

<span data-ttu-id="354f3-115">Usuwa aplikację z dzierżawy o identyfikatorze aplikacji "f9c5ea4f-28f0-401a-a491-491a037fa346".</span><span class="sxs-lookup"><span data-stu-id="354f3-115">Removes the application with application id 'f9c5ea4f-28f0-401a-a491-491a037fa346' from the tenant.</span></span>

### <span data-ttu-id="354f3-116">Przykład 3. Usuwanie aplikacji za pomocą rur</span><span class="sxs-lookup"><span data-stu-id="354f3-116">Example 3 - Remove application by piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738 | Remove-AzADApplication
```

<span data-ttu-id="354f3-117">Pobiera aplikację z identyfikatorem obiektu "b4cd1619-80b3-4cfb-9f8f-9f2333425738" i potokami, które są do polecenia cmdlet programu Remove-AzADApplication w celu usunięcia aplikacji z dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="354f3-117">Gets the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' and pipes that to the Remove-AzADApplication cmdlet to remove the application from the tenant.</span></span>

## <span data-ttu-id="354f3-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="354f3-118">PARAMETERS</span></span>

### <span data-ttu-id="354f3-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="354f3-119">-ApplicationId</span></span>
<span data-ttu-id="354f3-120">Identyfikator aplikacji do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="354f3-120">The application id of the application to remove.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="354f3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="354f3-121">-DefaultProfile</span></span>
<span data-ttu-id="354f3-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="354f3-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="354f3-123">— DisplayName</span><span class="sxs-lookup"><span data-stu-id="354f3-123">-DisplayName</span></span>
<span data-ttu-id="354f3-124">Nazwa wyświetlana aplikacji.</span><span class="sxs-lookup"><span data-stu-id="354f3-124">The display name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="354f3-125">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="354f3-125">-Force</span></span>
<span data-ttu-id="354f3-126">Przełącz się, aby usunąć aplikację bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="354f3-126">Switch to delete an application without a confirmation.</span></span>

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

### <span data-ttu-id="354f3-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="354f3-127">-InputObject</span></span>
<span data-ttu-id="354f3-128">Obiekt reprezentujący aplikację do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="354f3-128">The object representing the application to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="354f3-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="354f3-129">-ObjectId</span></span>
<span data-ttu-id="354f3-130">Identyfikator obiektu aplikacji do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="354f3-130">The object id of the application to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="354f3-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="354f3-131">-PassThru</span></span>
<span data-ttu-id="354f3-132">Określenie tej wartości spowoduje zwrócenie wartości prawda, jeśli polecenie zostało pomyślnie określone.</span><span class="sxs-lookup"><span data-stu-id="354f3-132">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="354f3-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="354f3-133">-Confirm</span></span>
<span data-ttu-id="354f3-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="354f3-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="354f3-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="354f3-135">-WhatIf</span></span>
<span data-ttu-id="354f3-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="354f3-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="354f3-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="354f3-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="354f3-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="354f3-138">CommonParameters</span></span>
<span data-ttu-id="354f3-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="354f3-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="354f3-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="354f3-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="354f3-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="354f3-141">INPUTS</span></span>

### <span data-ttu-id="354f3-142">System.String</span><span class="sxs-lookup"><span data-stu-id="354f3-142">System.String</span></span>

### <span data-ttu-id="354f3-143">System.Guid</span><span class="sxs-lookup"><span data-stu-id="354f3-143">System.Guid</span></span>

### <span data-ttu-id="354f3-144">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="354f3-144">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="354f3-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="354f3-145">OUTPUTS</span></span>

### <span data-ttu-id="354f3-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="354f3-146">System.Boolean</span></span>

## <span data-ttu-id="354f3-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="354f3-147">NOTES</span></span>
<span data-ttu-id="354f3-148">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, zasób, grupa, szablon, wdrożenie</span><span class="sxs-lookup"><span data-stu-id="354f3-148">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="354f3-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="354f3-149">RELATED LINKS</span></span>

[<span data-ttu-id="354f3-150">New-AzadApplication</span><span class="sxs-lookup"><span data-stu-id="354f3-150">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="354f3-151">Get-AzadApplication</span><span class="sxs-lookup"><span data-stu-id="354f3-151">Get-AzADApplication</span></span>](./Get-AzADApplication.md)


[<span data-ttu-id="354f3-152">Remove-AzadAppCredential</span><span class="sxs-lookup"><span data-stu-id="354f3-152">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

