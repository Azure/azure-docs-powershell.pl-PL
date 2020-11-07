---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C791C593-F7D5-4961-97F9-E4909813FFE7
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADApplication.md
ms.openlocfilehash: 00c9d6e5a5a729ca5a5119b812873078acb38326
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892445"
---
# <span data-ttu-id="1445d-101">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="1445d-101">Remove-AzADApplication</span></span>

## <span data-ttu-id="1445d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1445d-102">SYNOPSIS</span></span>
<span data-ttu-id="1445d-103">Usuwa aplikację Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1445d-103">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="1445d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1445d-104">SYNTAX</span></span>

### <span data-ttu-id="1445d-105">ObjectIdParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1445d-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADApplication -ObjectId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1445d-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1445d-106">ApplicationIdParameterSet</span></span>
```
Remove-AzADApplication -ApplicationId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1445d-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1445d-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzADApplication -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1445d-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1445d-108">InputObjectParameterSet</span></span>
```
Remove-AzADApplication -InputObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1445d-109">Opis</span><span class="sxs-lookup"><span data-stu-id="1445d-109">DESCRIPTION</span></span>
<span data-ttu-id="1445d-110">Usuwa aplikację Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1445d-110">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="1445d-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1445d-111">EXAMPLES</span></span>

### <span data-ttu-id="1445d-112">Przykład 1 — Usuwanie aplikacji według identyfikatora obiektu</span><span class="sxs-lookup"><span data-stu-id="1445d-112">Example 1 - Remove application by object id</span></span>

```
PS C:\> Remove-AzADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738
```

<span data-ttu-id="1445d-113">Usuwa aplikację z identyfikatorem obiektu "b4cd1619-80b3-4cfb-9f8f-9f2333425738" z dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="1445d-113">Removes the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' from the tenant.</span></span>

### <span data-ttu-id="1445d-114">Przykład 2 — Usuwanie aplikacji według identyfikatora aplikacji</span><span class="sxs-lookup"><span data-stu-id="1445d-114">Example 2 - Remove application by application id</span></span>

```
PS C:\> Remove-AzADApplication -ApplicationId f9c5ea4f-28f0-401a-a491-491a037fa346
```

<span data-ttu-id="1445d-115">Usuwa aplikację z identyfikatorem aplikacji "f9c5ea4f-28f0-401A-a491-491a037fa346" z dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="1445d-115">Removes the application with application id 'f9c5ea4f-28f0-401a-a491-491a037fa346' from the tenant.</span></span>

### <span data-ttu-id="1445d-116">Przykład 3-usunięcie aplikacji przez potok rurociągowy</span><span class="sxs-lookup"><span data-stu-id="1445d-116">Example 3 - Remove application by piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738 | Remove-AzADApplication
```

<span data-ttu-id="1445d-117">Pobiera aplikację o identyfikatorze obiektu "b4cd1619-80b3-4cfb-9f8f-9f2333425738" i potokach, które zostaną usunięte przez polecenie cmdlet Remove-AzADApplication w celu usunięcia aplikacji z dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="1445d-117">Gets the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' and pipes that to the Remove-AzADApplication cmdlet to remove the application from the tenant.</span></span>

## <span data-ttu-id="1445d-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1445d-118">PARAMETERS</span></span>

### <span data-ttu-id="1445d-119">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="1445d-119">-ApplicationId</span></span>
<span data-ttu-id="1445d-120">Identyfikator aplikacji, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="1445d-120">The application id of the application to remove.</span></span>

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

### <span data-ttu-id="1445d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1445d-121">-DefaultProfile</span></span>
<span data-ttu-id="1445d-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="1445d-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1445d-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="1445d-123">-DisplayName</span></span>
<span data-ttu-id="1445d-124">Nazwa wyświetlana aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1445d-124">The display name of the application.</span></span>

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

### <span data-ttu-id="1445d-125">-Force</span><span class="sxs-lookup"><span data-stu-id="1445d-125">-Force</span></span>
<span data-ttu-id="1445d-126">Przełączanie w celu usunięcia aplikacji bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="1445d-126">Switch to delete an application without a confirmation.</span></span>

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

### <span data-ttu-id="1445d-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1445d-127">-InputObject</span></span>
<span data-ttu-id="1445d-128">Obiekt reprezentujący aplikację do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="1445d-128">The object representing the application to remove.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1445d-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="1445d-129">-ObjectId</span></span>
<span data-ttu-id="1445d-130">Identyfikator obiektu aplikacji, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="1445d-130">The object id of the application to delete.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1445d-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1445d-131">-PassThru</span></span>
<span data-ttu-id="1445d-132">Określenie tej wartości zwróci wartość PRAWDA, jeśli polecenie zostało wykonane prawidłowo.</span><span class="sxs-lookup"><span data-stu-id="1445d-132">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="1445d-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1445d-133">-Confirm</span></span>
<span data-ttu-id="1445d-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1445d-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1445d-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1445d-135">-WhatIf</span></span>
<span data-ttu-id="1445d-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1445d-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1445d-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1445d-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1445d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1445d-138">CommonParameters</span></span>
<span data-ttu-id="1445d-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1445d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1445d-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1445d-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1445d-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1445d-141">INPUTS</span></span>

### <span data-ttu-id="1445d-142">System. GUID</span><span class="sxs-lookup"><span data-stu-id="1445d-142">System.Guid</span></span>

### <span data-ttu-id="1445d-143">System. String</span><span class="sxs-lookup"><span data-stu-id="1445d-143">System.String</span></span>

### <span data-ttu-id="1445d-144">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="1445d-144">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="1445d-145">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1445d-145">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="1445d-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1445d-146">OUTPUTS</span></span>

### <span data-ttu-id="1445d-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1445d-147">System.Boolean</span></span>

## <span data-ttu-id="1445d-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1445d-148">NOTES</span></span>
<span data-ttu-id="1445d-149">Słowa kluczowe: Azure, AZ, ramię, zasób, zarządzanie, Menedżer, zasób, Grupa, szablon, wdrożenie</span><span class="sxs-lookup"><span data-stu-id="1445d-149">Keywords: azure, Az, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="1445d-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1445d-150">RELATED LINKS</span></span>

[<span data-ttu-id="1445d-151">Nowe — AzADApplication</span><span class="sxs-lookup"><span data-stu-id="1445d-151">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="1445d-152">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="1445d-152">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="1445d-153">Set-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="1445d-153">Set-AzADApplication</span></span>](./Set-AzADApplication.md)

[<span data-ttu-id="1445d-154">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="1445d-154">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

