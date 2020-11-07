---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C791C593-F7D5-4961-97F9-E4909813FFE7
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADApplication.md
ms.openlocfilehash: eed437a235072972778925c0b94f2d22466399b3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708328"
---
# <span data-ttu-id="5214b-101">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="5214b-101">Remove-AzADApplication</span></span>

## <span data-ttu-id="5214b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5214b-102">SYNOPSIS</span></span>
<span data-ttu-id="5214b-103">Usuwa aplikację Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5214b-103">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="5214b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5214b-104">SYNTAX</span></span>

### <span data-ttu-id="5214b-105">ObjectIdParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5214b-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADApplication -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5214b-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5214b-106">ApplicationIdParameterSet</span></span>
```
Remove-AzADApplication -ApplicationId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5214b-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5214b-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzADApplication -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5214b-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5214b-108">InputObjectParameterSet</span></span>
```
Remove-AzADApplication -InputObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5214b-109">Opis</span><span class="sxs-lookup"><span data-stu-id="5214b-109">DESCRIPTION</span></span>
<span data-ttu-id="5214b-110">Usuwa aplikację Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5214b-110">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="5214b-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5214b-111">EXAMPLES</span></span>

### <span data-ttu-id="5214b-112">Przykład 1 — Usuwanie aplikacji według identyfikatora obiektu</span><span class="sxs-lookup"><span data-stu-id="5214b-112">Example 1 - Remove application by object id</span></span>

```
PS C:\> Remove-AzADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738
```

<span data-ttu-id="5214b-113">Usuwa aplikację z identyfikatorem obiektu "b4cd1619-80b3-4cfb-9f8f-9f2333425738" z dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="5214b-113">Removes the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' from the tenant.</span></span>

### <span data-ttu-id="5214b-114">Przykład 2 — Usuwanie aplikacji według identyfikatora aplikacji</span><span class="sxs-lookup"><span data-stu-id="5214b-114">Example 2 - Remove application by application id</span></span>

```
PS C:\> Remove-AzADApplication -ApplicationId f9c5ea4f-28f0-401a-a491-491a037fa346
```

<span data-ttu-id="5214b-115">Usuwa aplikację z identyfikatorem aplikacji "f9c5ea4f-28f0-401A-a491-491a037fa346" z dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="5214b-115">Removes the application with application id 'f9c5ea4f-28f0-401a-a491-491a037fa346' from the tenant.</span></span>

### <span data-ttu-id="5214b-116">Przykład 3-usunięcie aplikacji przez potok rurociągowy</span><span class="sxs-lookup"><span data-stu-id="5214b-116">Example 3 - Remove application by piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738 | Remove-AzADApplication
```

<span data-ttu-id="5214b-117">Pobiera aplikację o identyfikatorze obiektu "b4cd1619-80b3-4cfb-9f8f-9f2333425738" i potokach, które zostaną usunięte przez polecenie cmdlet Remove-AzADApplication w celu usunięcia aplikacji z dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="5214b-117">Gets the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' and pipes that to the Remove-AzADApplication cmdlet to remove the application from the tenant.</span></span>

## <span data-ttu-id="5214b-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5214b-118">PARAMETERS</span></span>

### <span data-ttu-id="5214b-119">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="5214b-119">-ApplicationId</span></span>
<span data-ttu-id="5214b-120">Identyfikator aplikacji, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="5214b-120">The application id of the application to remove.</span></span>

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

### <span data-ttu-id="5214b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5214b-121">-DefaultProfile</span></span>
<span data-ttu-id="5214b-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="5214b-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5214b-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="5214b-123">-DisplayName</span></span>
<span data-ttu-id="5214b-124">Nazwa wyświetlana aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5214b-124">The display name of the application.</span></span>

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

### <span data-ttu-id="5214b-125">-Force</span><span class="sxs-lookup"><span data-stu-id="5214b-125">-Force</span></span>
<span data-ttu-id="5214b-126">Przełączanie w celu usunięcia aplikacji bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="5214b-126">Switch to delete an application without a confirmation.</span></span>

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

### <span data-ttu-id="5214b-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5214b-127">-InputObject</span></span>
<span data-ttu-id="5214b-128">Obiekt reprezentujący aplikację do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="5214b-128">The object representing the application to remove.</span></span>

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

### <span data-ttu-id="5214b-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="5214b-129">-ObjectId</span></span>
<span data-ttu-id="5214b-130">Identyfikator obiektu aplikacji, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="5214b-130">The object id of the application to delete.</span></span>

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

### <span data-ttu-id="5214b-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5214b-131">-PassThru</span></span>
<span data-ttu-id="5214b-132">Określenie tej wartości zwróci wartość PRAWDA, jeśli polecenie zostało wykonane prawidłowo.</span><span class="sxs-lookup"><span data-stu-id="5214b-132">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="5214b-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5214b-133">-Confirm</span></span>
<span data-ttu-id="5214b-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5214b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5214b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5214b-135">-WhatIf</span></span>
<span data-ttu-id="5214b-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5214b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5214b-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5214b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5214b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5214b-138">CommonParameters</span></span>
<span data-ttu-id="5214b-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5214b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5214b-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5214b-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5214b-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5214b-141">INPUTS</span></span>

### <span data-ttu-id="5214b-142">System. String</span><span class="sxs-lookup"><span data-stu-id="5214b-142">System.String</span></span>

### <span data-ttu-id="5214b-143">System. GUID</span><span class="sxs-lookup"><span data-stu-id="5214b-143">System.Guid</span></span>

### <span data-ttu-id="5214b-144">Microsoft. Azure. Commands. pozycji. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="5214b-144">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="5214b-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5214b-145">OUTPUTS</span></span>

### <span data-ttu-id="5214b-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5214b-146">System.Boolean</span></span>

## <span data-ttu-id="5214b-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5214b-147">NOTES</span></span>
<span data-ttu-id="5214b-148">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, zasób, Grupa, szablon, wdrożenie</span><span class="sxs-lookup"><span data-stu-id="5214b-148">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="5214b-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5214b-149">RELATED LINKS</span></span>

[<span data-ttu-id="5214b-150">Nowe — AzADApplication</span><span class="sxs-lookup"><span data-stu-id="5214b-150">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="5214b-151">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="5214b-151">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="5214b-152">Set-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="5214b-152">Set-AzADApplication</span></span>](./Set-AzADApplication.md)

[<span data-ttu-id="5214b-153">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="5214b-153">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

