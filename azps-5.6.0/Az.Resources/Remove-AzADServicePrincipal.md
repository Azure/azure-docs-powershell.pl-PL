---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0C8C07CA-6720-452F-A952-48C76EBF3BBD
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADServicePrincipal.md
ms.openlocfilehash: e9e4a8e902b3d71507a9e9d731ceb518825f8aa6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970353"
---
# <span data-ttu-id="c2884-101">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c2884-101">Remove-AzADServicePrincipal</span></span>

## <span data-ttu-id="c2884-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2884-102">SYNOPSIS</span></span>
<span data-ttu-id="c2884-103">Usuwa podmiot zabezpieczeń usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c2884-103">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="c2884-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c2884-104">SYNTAX</span></span>

### <span data-ttu-id="c2884-105">ObjectIdParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="c2884-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADServicePrincipal -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2884-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2884-106">ApplicationIdParameterSet</span></span>
```
Remove-AzADServicePrincipal -ApplicationId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2884-107">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2884-107">SPNParameterSet</span></span>
```
Remove-AzADServicePrincipal -ServicePrincipalName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2884-108">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2884-108">DisplayNameParameterSet</span></span>
```
Remove-AzADServicePrincipal -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2884-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2884-109">InputObjectParameterSet</span></span>
```
Remove-AzADServicePrincipal -InputObject <PSADServicePrincipal> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2884-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2884-110">ApplicationObjectParameterSet</span></span>
```
Remove-AzADServicePrincipal -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2884-111">OPIS</span><span class="sxs-lookup"><span data-stu-id="c2884-111">DESCRIPTION</span></span>
<span data-ttu-id="c2884-112">Usuwa podmiot zabezpieczeń usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c2884-112">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="c2884-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c2884-113">EXAMPLES</span></span>

### <span data-ttu-id="c2884-114">Przykład 1. Usuwanie podmiotu zabezpieczeń usługi według identyfikatora obiektu</span><span class="sxs-lookup"><span data-stu-id="c2884-114">Example 1 - Remove a service principal by object id</span></span>

```
PS C:\> Remove-AzADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45
```

<span data-ttu-id="c2884-115">Usuwa podmiot zabezpieczeń usługi z identyfikatorem obiektu '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45'.</span><span class="sxs-lookup"><span data-stu-id="c2884-115">Removes the service principal with object id '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45'.</span></span>

### <span data-ttu-id="c2884-116">Przykład 2. Usuwanie podmiotu zabezpieczeń usługi według identyfikatora aplikacji</span><span class="sxs-lookup"><span data-stu-id="c2884-116">Example 2 - Remove a service principal by application id</span></span>

```
PS C:\> Remove-AzADServicePrincipal -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76
```

<span data-ttu-id="c2884-117">Usuwa podmiot zabezpieczeń usługi z identyfikatorem aplikacji '9263469e-d328-4321-8646-3e3e75d20e76".</span><span class="sxs-lookup"><span data-stu-id="c2884-117">Removes the service principal with application id '9263469e-d328-4321-8646-3e3e75d20e76'.</span></span>

### <span data-ttu-id="c2884-118">Przykład 3. Usuwanie podmiotu zabezpieczeń usługi przez dodatek SPN</span><span class="sxs-lookup"><span data-stu-id="c2884-118">Example 3 - Remove a service principal by SPN</span></span>

```
PS C:\> Remove-AzADServicePrincipal -ServicePrincipalName MyServicePrincipal
```

<span data-ttu-id="c2884-119">Usuwanie podmiotu zabezpieczeń usługi przy użyciu nazwy głównej usługi "MyServicePrincipal"</span><span class="sxs-lookup"><span data-stu-id="c2884-119">Remove the service principal with service principal name "MyServicePrincipal"</span></span>

### <span data-ttu-id="c2884-120">Przykład 4. Usuwanie podmiotu zabezpieczeń usługi za pomocą funkcji pipingu</span><span class="sxs-lookup"><span data-stu-id="c2884-120">Example 4 - Remove a service principal by piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45 | Remove-AzADServicePrincipal
```

<span data-ttu-id="c2884-121">Pobiera podmiot zabezpieczeń usługi z identyfikatorem obiektu "61b5d8ea-fdc6-40a2-8d5b-ad447c678d45" i potoki, które są do polecenia cmdlet programu Remove-AzADServicePrincipal w celu usunięcia tego podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="c2884-121">Gets the service principal with object id '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45' and pipes that to the Remove-AzADServicePrincipal cmdlet to remove that service principal.</span></span>

### <span data-ttu-id="c2884-122">Przykład 5. Usuwanie podmiotu zabezpieczeń usługi przez stosowanie rur</span><span class="sxs-lookup"><span data-stu-id="c2884-122">Example 5 - Remove a service principal by piping an application</span></span>

```
PS C:\> Get-AzApplication -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76 | Remove-AzADServicePrincipal
```

<span data-ttu-id="c2884-123">Pobiera aplikację z identyfikatorem aplikacji "9263469e-d328-4321-8646-3e3e75d20e76" i potokami, które są przekierowywowane do polecenia cmdlet programu Remove-AzADServicePrincipal w celu usunięcia podmiotu zabezpieczeń usługi skojarzonego z tą aplikacją.</span><span class="sxs-lookup"><span data-stu-id="c2884-123">Gets the application with application id '9263469e-d328-4321-8646-3e3e75d20e76' and pipes that to the Remove-AzADServicePrincipal cmdlet to remove the service principal associated with that application.</span></span>

## <span data-ttu-id="c2884-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c2884-124">PARAMETERS</span></span>

### <span data-ttu-id="c2884-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="c2884-125">-ApplicationId</span></span>
<span data-ttu-id="c2884-126">Identyfikator aplikacji podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="c2884-126">The service principal application id.</span></span>

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

### <span data-ttu-id="c2884-127">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="c2884-127">-ApplicationObject</span></span>
<span data-ttu-id="c2884-128">Obiekt aplikacji, którego podmiot zabezpieczeń usługi jest usuwany.</span><span class="sxs-lookup"><span data-stu-id="c2884-128">The application object whose service principal is being removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2884-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2884-129">-DefaultProfile</span></span>
<span data-ttu-id="c2884-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="c2884-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c2884-131">— DisplayName</span><span class="sxs-lookup"><span data-stu-id="c2884-131">-DisplayName</span></span>
<span data-ttu-id="c2884-132">Nazwa wyświetlana podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="c2884-132">The display name of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2884-133">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="c2884-133">-Force</span></span>
<span data-ttu-id="c2884-134">Przełączanie w celu usunięcia podmiotu zabezpieczeń usługi bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="c2884-134">Switch to delete service principal without a confirmation.</span></span>

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

### <span data-ttu-id="c2884-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2884-135">-InputObject</span></span>
<span data-ttu-id="c2884-136">Obiekt podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="c2884-136">The service principal object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2884-137">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="c2884-137">-ObjectId</span></span>
<span data-ttu-id="c2884-138">Identyfikator obiektu podmiotu zabezpieczeń usługi do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="c2884-138">The object id of the service principal to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases: PrincipalId, Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2884-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c2884-139">-PassThru</span></span>
<span data-ttu-id="c2884-140">Jeśli jest to określone, zwraca usunięty podmiot zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="c2884-140">If specified, returns the deleted service principal.</span></span>

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

### <span data-ttu-id="c2884-141">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="c2884-141">-ServicePrincipalName</span></span>
<span data-ttu-id="c2884-142">Nazwa podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="c2884-142">The service principal name.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2884-143">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c2884-143">-Confirm</span></span>
<span data-ttu-id="c2884-144">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c2884-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2884-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2884-145">-WhatIf</span></span>
<span data-ttu-id="c2884-146">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2884-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2884-147">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c2884-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2884-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2884-148">CommonParameters</span></span>
<span data-ttu-id="c2884-149">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2884-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2884-150">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c2884-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2884-151">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c2884-151">INPUTS</span></span>

### <span data-ttu-id="c2884-152">System.String</span><span class="sxs-lookup"><span data-stu-id="c2884-152">System.String</span></span>

### <span data-ttu-id="c2884-153">System.Guid</span><span class="sxs-lookup"><span data-stu-id="c2884-153">System.Guid</span></span>

### <span data-ttu-id="c2884-154">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c2884-154">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="c2884-155">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="c2884-155">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="c2884-156">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c2884-156">OUTPUTS</span></span>

### <span data-ttu-id="c2884-157">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c2884-157">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="c2884-158">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c2884-158">NOTES</span></span>
<span data-ttu-id="c2884-159">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, zasób, grupa, szablon, wdrożenie</span><span class="sxs-lookup"><span data-stu-id="c2884-159">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="c2884-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c2884-160">RELATED LINKS</span></span>

[<span data-ttu-id="c2884-161">New-AzadServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c2884-161">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)

[<span data-ttu-id="c2884-162">Get-AzadServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c2884-162">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="c2884-163">Update-AzadServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c2884-163">Update-AzADServicePrincipal</span></span>](./Update-AzADServicePrincipal.md)

[<span data-ttu-id="c2884-164">Remove-AzadApplication</span><span class="sxs-lookup"><span data-stu-id="c2884-164">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="c2884-165">Remove-AzadAppCredential</span><span class="sxs-lookup"><span data-stu-id="c2884-165">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)
