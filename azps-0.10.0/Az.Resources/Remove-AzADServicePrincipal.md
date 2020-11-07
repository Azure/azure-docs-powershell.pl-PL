---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0C8C07CA-6720-452F-A952-48C76EBF3BBD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADServicePrincipal.md
ms.openlocfilehash: 966b9baf35f1719f29fda6355a9675739693314f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892437"
---
# <span data-ttu-id="ac7eb-101">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="ac7eb-101">Remove-AzADServicePrincipal</span></span>

## <span data-ttu-id="ac7eb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ac7eb-102">SYNOPSIS</span></span>
<span data-ttu-id="ac7eb-103">Usuwa podmiot zabezpieczeń usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ac7eb-103">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="ac7eb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ac7eb-104">SYNTAX</span></span>

### <span data-ttu-id="ac7eb-105">ObjectIdParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ac7eb-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADServicePrincipal -ObjectId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac7eb-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac7eb-106">ApplicationIdParameterSet</span></span>
```
Remove-AzADServicePrincipal -ApplicationId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac7eb-107">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac7eb-107">SPNParameterSet</span></span>
```
Remove-AzADServicePrincipal -ServicePrincipalName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac7eb-108">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac7eb-108">DisplayNameParameterSet</span></span>
```
Remove-AzADServicePrincipal -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac7eb-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac7eb-109">InputObjectParameterSet</span></span>
```
Remove-AzADServicePrincipal -InputObject <PSADServicePrincipal> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac7eb-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac7eb-110">ApplicationObjectParameterSet</span></span>
```
Remove-AzADServicePrincipal -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac7eb-111">Opis</span><span class="sxs-lookup"><span data-stu-id="ac7eb-111">DESCRIPTION</span></span>
<span data-ttu-id="ac7eb-112">Usuwa podmiot zabezpieczeń usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ac7eb-112">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="ac7eb-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ac7eb-113">EXAMPLES</span></span>

### <span data-ttu-id="ac7eb-114">Przykład 1 — Usuwanie podmiotu zabezpieczeń usługi według identyfikatora obiektu</span><span class="sxs-lookup"><span data-stu-id="ac7eb-114">Example 1 - Remove a service principal by object id</span></span>

```
PS C:\> Remove-AzADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45
```

<span data-ttu-id="ac7eb-115">Usuwa podmiot zabezpieczeń usługi z identyfikatorem obiektu "61b5d8ea-fdc6-40a2-8d5b-ad447c678d45".</span><span class="sxs-lookup"><span data-stu-id="ac7eb-115">Removes the service principal with object id '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45'.</span></span>

### <span data-ttu-id="ac7eb-116">Przykład 2 — Usuwanie podmiotu zabezpieczeń usługi według identyfikatora aplikacji</span><span class="sxs-lookup"><span data-stu-id="ac7eb-116">Example 2 - Remove a service principal by application id</span></span>

```
PS C:\> Remove-AzADServicePrincipal -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76
```

<span data-ttu-id="ac7eb-117">Usuwa podmiot zabezpieczeń usługi z identyfikatorem aplikacji "9263469e-d328-4321-8646-3e3e75d20e76".</span><span class="sxs-lookup"><span data-stu-id="ac7eb-117">Removes the service principal with application id '9263469e-d328-4321-8646-3e3e75d20e76'.</span></span>

### <span data-ttu-id="ac7eb-118">Przykład 3 — Usuwanie podmiotu zabezpieczeń usługi według nazwy SPN</span><span class="sxs-lookup"><span data-stu-id="ac7eb-118">Example 3 - Remove a service principal by SPN</span></span>

```
PS C:\> Remove-AzADServicePrincipal -ServicePrincipalName MyServicePrincipal
```

<span data-ttu-id="ac7eb-119">Usuwanie podmiotu usługi z nazwą główną usługi "MyServicePrincipal"</span><span class="sxs-lookup"><span data-stu-id="ac7eb-119">Remove the service principal with service principal name "MyServicePrincipal"</span></span>

### <span data-ttu-id="ac7eb-120">Przykład 4 — Usuwanie podmiotu zabezpieczeń usługi według połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="ac7eb-120">Example 4 - Remove a service principal by piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45 | Remove-AzADServicePrincipal
```

<span data-ttu-id="ac7eb-121">Pobiera podmiot zabezpieczeń usługi o identyfikatorze obiektu "61b5d8ea-fdc6-40a2-8d5b-ad447c678d45" i potokach, które zostaną usunięte przez polecenie cmdlet Remove-AzADServicePrincipal w celu usunięcia tego podmiotu usługi.</span><span class="sxs-lookup"><span data-stu-id="ac7eb-121">Gets the service principal with object id '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45' and pipes that to the Remove-AzADServicePrincipal cmdlet to remove that service principal.</span></span>

### <span data-ttu-id="ac7eb-122">Przykład 5 — Usuwanie podmiotu usługi przez potok aplikacji</span><span class="sxs-lookup"><span data-stu-id="ac7eb-122">Example 5 - Remove a service principal by piping an application</span></span>

```
PS C:\> Get-AzApplication -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76 | Remove-AzADServicePrincipal
```

<span data-ttu-id="ac7eb-123">Pobiera aplikację o identyfikatorze aplikacji "9263469e-d328-4321-8646-3e3e75d20e76" i potokach, które zostaną usunięte przez polecenie cmdlet Remove-AzADServicePrincipal w celu usunięcia podmiotu usługi skojarzonego z tą aplikacją.</span><span class="sxs-lookup"><span data-stu-id="ac7eb-123">Gets the application with application id '9263469e-d328-4321-8646-3e3e75d20e76' and pipes that to the Remove-AzADServicePrincipal cmdlet to remove the service principal associated with that application.</span></span>

## <span data-ttu-id="ac7eb-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ac7eb-124">PARAMETERS</span></span>

### <span data-ttu-id="ac7eb-125">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="ac7eb-125">-ApplicationId</span></span>
<span data-ttu-id="ac7eb-126">Identyfikator głównej aplikacji usługi.</span><span class="sxs-lookup"><span data-stu-id="ac7eb-126">The service principal application id.</span></span>

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

### <span data-ttu-id="ac7eb-127">-Applicationobject</span><span class="sxs-lookup"><span data-stu-id="ac7eb-127">-ApplicationObject</span></span>
<span data-ttu-id="ac7eb-128">Obiekt aplikacji, którego podmiot usługi jest usuwany.</span><span class="sxs-lookup"><span data-stu-id="ac7eb-128">The application object whose service principal is being removed.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac7eb-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac7eb-129">-DefaultProfile</span></span>
<span data-ttu-id="ac7eb-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="ac7eb-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac7eb-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ac7eb-131">-DisplayName</span></span>
<span data-ttu-id="ac7eb-132">Nazwa wyświetlana podmiotu usługi.</span><span class="sxs-lookup"><span data-stu-id="ac7eb-132">The display name of the service principal.</span></span>

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

### <span data-ttu-id="ac7eb-133">-Force</span><span class="sxs-lookup"><span data-stu-id="ac7eb-133">-Force</span></span>
<span data-ttu-id="ac7eb-134">Przełączanie do Usuń podmiot zabezpieczeń usługi bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="ac7eb-134">Switch to delete service principal without a confirmation.</span></span>

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

### <span data-ttu-id="ac7eb-135">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ac7eb-135">-InputObject</span></span>
<span data-ttu-id="ac7eb-136">Główny obiekt usługi.</span><span class="sxs-lookup"><span data-stu-id="ac7eb-136">The service principal object.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac7eb-137">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="ac7eb-137">-ObjectId</span></span>
<span data-ttu-id="ac7eb-138">Identyfikator obiektu podmiotu usługi, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="ac7eb-138">The object id of the service principal to delete.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases: PrincipalId, Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac7eb-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ac7eb-139">-PassThru</span></span>
<span data-ttu-id="ac7eb-140">Jeśli ta funkcja jest określona, zwraca usunięty podmiot zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="ac7eb-140">If specified, returns the deleted service principal.</span></span>

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

### <span data-ttu-id="ac7eb-141">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="ac7eb-141">-ServicePrincipalName</span></span>
<span data-ttu-id="ac7eb-142">Nazwa główna usługi.</span><span class="sxs-lookup"><span data-stu-id="ac7eb-142">The service principal name.</span></span>

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

### <span data-ttu-id="ac7eb-143">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ac7eb-143">-Confirm</span></span>
<span data-ttu-id="ac7eb-144">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac7eb-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac7eb-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac7eb-145">-WhatIf</span></span>
<span data-ttu-id="ac7eb-146">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac7eb-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac7eb-147">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ac7eb-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac7eb-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac7eb-148">CommonParameters</span></span>
<span data-ttu-id="ac7eb-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac7eb-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac7eb-150">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac7eb-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac7eb-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ac7eb-151">INPUTS</span></span>

### <span data-ttu-id="ac7eb-152">System. GUID</span><span class="sxs-lookup"><span data-stu-id="ac7eb-152">System.Guid</span></span>

### <span data-ttu-id="ac7eb-153">System. String</span><span class="sxs-lookup"><span data-stu-id="ac7eb-153">System.String</span></span>

### <span data-ttu-id="ac7eb-154">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="ac7eb-154">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>
<span data-ttu-id="ac7eb-155">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ac7eb-155">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="ac7eb-156">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="ac7eb-156">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="ac7eb-157">Parametry: Applicationobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ac7eb-157">Parameters: ApplicationObject (ByValue)</span></span>

## <span data-ttu-id="ac7eb-158">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ac7eb-158">OUTPUTS</span></span>

### <span data-ttu-id="ac7eb-159">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="ac7eb-159">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="ac7eb-160">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ac7eb-160">NOTES</span></span>
<span data-ttu-id="ac7eb-161">Słowa kluczowe: Azure, AZ, ramię, zasób, zarządzanie, Menedżer, zasób, Grupa, szablon, wdrożenie</span><span class="sxs-lookup"><span data-stu-id="ac7eb-161">Keywords: azure, Az, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="ac7eb-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ac7eb-162">RELATED LINKS</span></span>

[<span data-ttu-id="ac7eb-163">Nowe — AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="ac7eb-163">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)

[<span data-ttu-id="ac7eb-164">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="ac7eb-164">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="ac7eb-165">Set-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="ac7eb-165">Set-AzADServicePrincipal</span></span>](./Set-AzADServicePrincipal.md)

[<span data-ttu-id="ac7eb-166">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="ac7eb-166">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="ac7eb-167">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="ac7eb-167">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)
