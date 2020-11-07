---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C61FA834-BEBE-4DBF-888F-C6CB8CC95390
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadappcredential
schema: 2.0.0
ms.openlocfilehash: 0e442687604b99249f7e64a1c6d1fd4db91c38b9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899030"
---
# <span data-ttu-id="49ef3-101">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="49ef3-101">Remove-AzureRmADAppCredential</span></span>

## <span data-ttu-id="49ef3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="49ef3-102">SYNOPSIS</span></span>
<span data-ttu-id="49ef3-103">Usuwa poświadczenie z aplikacji.</span><span class="sxs-lookup"><span data-stu-id="49ef3-103">Removes a credential from an application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49ef3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="49ef3-104">SYNTAX</span></span>

### <span data-ttu-id="49ef3-105">ApplicationObjectIdWithKeyIdParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="49ef3-105">ApplicationObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzureRmADAppCredential -ObjectId <Guid> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49ef3-106">ApplicationIdWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="49ef3-106">ApplicationIdWithKeyIdParameterSet</span></span>
```
Remove-AzureRmADAppCredential -ApplicationId <Guid> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49ef3-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="49ef3-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzureRmADAppCredential -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49ef3-108">ApplicationObjectWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="49ef3-108">ApplicationObjectWithKeyIdParameterSet</span></span>
```
Remove-AzureRmADAppCredential [-KeyId <Guid>] -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49ef3-109">Opis</span><span class="sxs-lookup"><span data-stu-id="49ef3-109">DESCRIPTION</span></span>
<span data-ttu-id="49ef3-110">Polecenia cmdlet Remove-AzureRmADAppCredential można użyć w celu usunięcia klucza poświadczeń z aplikacji w przypadku złamania zabezpieczeń lub w ramach wygaśnięcia klucza poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="49ef3-110">The Remove-AzureRmADAppCredential cmdlet can be used to remove a credential key from an application in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="49ef3-111">Aplikacja jest identyfikowana przez podanie identyfikatora obiektu lub identyfikatora aplikacji.</span><span class="sxs-lookup"><span data-stu-id="49ef3-111">The application is identified by supplying either the object ID or AppId.</span></span>
<span data-ttu-id="49ef3-112">Poświadczenie, które ma zostać usunięte, jest identyfikowane za pomocą identyfikatora klucza.</span><span class="sxs-lookup"><span data-stu-id="49ef3-112">The credential to be removed is identified by its key ID.</span></span>

## <span data-ttu-id="49ef3-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="49ef3-113">EXAMPLES</span></span>

### <span data-ttu-id="49ef3-114">Przykład 1 — Usuwanie konkretnego poświadczenia z aplikacji</span><span class="sxs-lookup"><span data-stu-id="49ef3-114">Example 1 - Remove a specific credential from an application</span></span>

```
PS C:\> Remove-AzureRmADAppCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="49ef3-115">Usuwa poświadczenie o identyfikatorze klucza "9044423a-60a3-45ac-9ab1-09534157ebb" z aplikacji z identyfikatorem obiektu "7663d3fb-6f86-4352-9E6D-cf9d50d5ee82".</span><span class="sxs-lookup"><span data-stu-id="49ef3-115">Removes the credential with key id '9044423a-60a3-45ac-9ab1-09534157ebb' from the application with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span></span>

### <span data-ttu-id="49ef3-116">Przykład 2 — Usuwanie wszystkich poświadczeń z aplikacji</span><span class="sxs-lookup"><span data-stu-id="49ef3-116">Example 2 - Remove all credentials from an application</span></span>

```
PS C:\> Remove-AzureRmADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58
```

<span data-ttu-id="49ef3-117">Usuwa wszystkie poświadczenia z aplikacji z identyfikatorem aplikacji "4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58".</span><span class="sxs-lookup"><span data-stu-id="49ef3-117">Removes all credentials from the application with application id '4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58'.</span></span>

### <span data-ttu-id="49ef3-118">Przykład 3-Usuwanie wszystkich poświadczeń przy użyciu połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="49ef3-118">Example 3 - Remove all credentials using piping</span></span>

```
PS C:\> Get-AzureRmADApplication -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 | Remove-AzureRmADAppCredential
```

<span data-ttu-id="49ef3-119">Pobiera aplikację o identyfikatorze obiektu "7663d3fb-6f86-4352-9E6D-cf9d50d5ee82" i potokach, które zostaną usunięte przez polecenie cmdlet Remove-AzureRmADAppCredential i usuwa wszystkie poświadczenia z tej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="49ef3-119">Gets the application with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82' and pipes that to the Remove-AzureRmADAppCredential cmdlet and removes all credentials from that application.</span></span>

## <span data-ttu-id="49ef3-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="49ef3-120">PARAMETERS</span></span>

### <span data-ttu-id="49ef3-121">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="49ef3-121">-ApplicationId</span></span>
<span data-ttu-id="49ef3-122">Identyfikator aplikacji, z której mają zostać usunięte poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="49ef3-122">The id of the application to remove the credentials from.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49ef3-123">-Applicationobject</span><span class="sxs-lookup"><span data-stu-id="49ef3-123">-ApplicationObject</span></span>
<span data-ttu-id="49ef3-124">Obiekt aplikacji, z którego mają zostać usunięte poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="49ef3-124">The application object to remove the credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49ef3-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49ef3-125">-DefaultProfile</span></span>
<span data-ttu-id="49ef3-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="49ef3-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="49ef3-127">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="49ef3-127">-DisplayName</span></span>
<span data-ttu-id="49ef3-128">Nazwa wyświetlana aplikacji.</span><span class="sxs-lookup"><span data-stu-id="49ef3-128">The display name of the application.</span></span>

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

### <span data-ttu-id="49ef3-129">-Force</span><span class="sxs-lookup"><span data-stu-id="49ef3-129">-Force</span></span>
<span data-ttu-id="49ef3-130">Przełączanie do usuwania poświadczenia bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="49ef3-130">Switch to delete credential without a confirmation.</span></span>

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

### <span data-ttu-id="49ef3-131">-KeyId</span><span class="sxs-lookup"><span data-stu-id="49ef3-131">-KeyId</span></span>
<span data-ttu-id="49ef3-132">Określa klucz poświadczenia, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="49ef3-132">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="49ef3-133">Identyfikatory kluczy aplikacji można uzyskać przy użyciu polecenia cmdlet Get-AzureRmADAppCredential.</span><span class="sxs-lookup"><span data-stu-id="49ef3-133">The key Ids for the application can be obtained using the Get-AzureRmADAppCredential cmdlet.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet, ApplicationIdWithKeyIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectWithKeyIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49ef3-134">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="49ef3-134">-ObjectId</span></span>
<span data-ttu-id="49ef3-135">Identyfikator obiektu aplikacji, z którego mają zostać usunięte poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="49ef3-135">The object id of the application to remove the credentials from.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49ef3-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="49ef3-136">-PassThru</span></span>
<span data-ttu-id="49ef3-137">Określenie tej wartości zwróci wartość PRAWDA, jeśli polecenie zostało wykonane prawidłowo.</span><span class="sxs-lookup"><span data-stu-id="49ef3-137">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="49ef3-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="49ef3-138">-Confirm</span></span>
<span data-ttu-id="49ef3-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49ef3-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49ef3-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49ef3-140">-WhatIf</span></span>
<span data-ttu-id="49ef3-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49ef3-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49ef3-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="49ef3-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49ef3-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49ef3-143">CommonParameters</span></span>
<span data-ttu-id="49ef3-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49ef3-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49ef3-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49ef3-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49ef3-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="49ef3-146">INPUTS</span></span>

### <span data-ttu-id="49ef3-147">System. GUID</span><span class="sxs-lookup"><span data-stu-id="49ef3-147">System.Guid</span></span>

### <span data-ttu-id="49ef3-148">System. String</span><span class="sxs-lookup"><span data-stu-id="49ef3-148">System.String</span></span>

### <span data-ttu-id="49ef3-149">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="49ef3-149">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="49ef3-150">Parametry: Applicationobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="49ef3-150">Parameters: ApplicationObject (ByValue)</span></span>

## <span data-ttu-id="49ef3-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="49ef3-151">OUTPUTS</span></span>

### <span data-ttu-id="49ef3-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="49ef3-152">System.Boolean</span></span>

## <span data-ttu-id="49ef3-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="49ef3-153">NOTES</span></span>

## <span data-ttu-id="49ef3-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="49ef3-154">RELATED LINKS</span></span>

[<span data-ttu-id="49ef3-155">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="49ef3-155">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="49ef3-156">Nowe — AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="49ef3-156">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="49ef3-157">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="49ef3-157">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)
