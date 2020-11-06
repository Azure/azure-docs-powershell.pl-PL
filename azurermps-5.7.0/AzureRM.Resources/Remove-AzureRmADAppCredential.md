---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C61FA834-BEBE-4DBF-888F-C6CB8CC95390
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADAppCredential.md
ms.openlocfilehash: 0cfcb2713eaac255f625b09c0ba81883242f48aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526613"
---
# <span data-ttu-id="645db-101">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="645db-101">Remove-AzureRmADAppCredential</span></span>

## <span data-ttu-id="645db-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="645db-102">SYNOPSIS</span></span>
<span data-ttu-id="645db-103">Usuwa poświadczenie z aplikacji.</span><span class="sxs-lookup"><span data-stu-id="645db-103">Removes a credential from an application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="645db-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="645db-104">SYNTAX</span></span>

### <span data-ttu-id="645db-105">ApplicationObjectIdWithKeyIdParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="645db-105">ApplicationObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzureRmADAppCredential -ObjectId <String> -KeyId <Guid> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="645db-106">ApplicationObjectIdWithAllParameterSet</span><span class="sxs-lookup"><span data-stu-id="645db-106">ApplicationObjectIdWithAllParameterSet</span></span>
```
Remove-AzureRmADAppCredential -ObjectId <String> [-All] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="645db-107">ApplicationIdWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="645db-107">ApplicationIdWithKeyIdParameterSet</span></span>
```
Remove-AzureRmADAppCredential -ApplicationId <String> -KeyId <Guid> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="645db-108">ApplicationIdWithAllParameterSet</span><span class="sxs-lookup"><span data-stu-id="645db-108">ApplicationIdWithAllParameterSet</span></span>
```
Remove-AzureRmADAppCredential -ApplicationId <String> [-All] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="645db-109">Opis</span><span class="sxs-lookup"><span data-stu-id="645db-109">DESCRIPTION</span></span>
<span data-ttu-id="645db-110">Polecenia cmdlet Remove-AzureRmADAppCredential można użyć w celu usunięcia klucza poświadczeń z aplikacji w przypadku złamania zabezpieczeń lub w ramach wygaśnięcia klucza poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="645db-110">The Remove-AzureRmADAppCredential cmdlet can be used to remove a credential key from an application in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="645db-111">Aplikacja jest identyfikowana przez podanie identyfikatora obiektu lub identyfikatora aplikacji.</span><span class="sxs-lookup"><span data-stu-id="645db-111">The application is identified by supplying either the object ID or AppId.</span></span>
<span data-ttu-id="645db-112">Poświadczenie, które ma zostać usunięte, jest identyfikowane za pomocą identyfikatora klucza, jeśli pojedyncze poświadczenie zostanie usunięte lub z przełącznikiem wszystkie, w celu usunięcia wszystkich poświadczeń skojarzonych z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="645db-112">The credential to be removed is identified by its key ID if an individual credential is to be removed or with an 'All' switch to delete all credentials associated with the application.</span></span>

## <span data-ttu-id="645db-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="645db-113">EXAMPLES</span></span>

### <span data-ttu-id="645db-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="645db-114">Example 1</span></span>
```
PS E:\> Remove-AzureRmADAppCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="645db-115">To polecenie usuwa klucz poświadczenia z aplikacji.</span><span class="sxs-lookup"><span data-stu-id="645db-115">This command removes a credential key from an application.</span></span>
<span data-ttu-id="645db-116">W tym przykładzie klucz z identyfikatorem "9044423a-60a3-45ac-9ab1-09534157ebb" zostanie usunięty z aplikacji.</span><span class="sxs-lookup"><span data-stu-id="645db-116">In this example, the key with Id "9044423a-60a3-45ac-9ab1-09534157ebb" will be removed from the application.</span></span>

### <span data-ttu-id="645db-117">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="645db-117">Example 2</span></span>
```
PS E:\> Remove-AzureRmADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 -All
```

<span data-ttu-id="645db-118">To polecenie usuwa klucz poświadczenia z aplikacji.</span><span class="sxs-lookup"><span data-stu-id="645db-118">This command removes a credential key from an application.</span></span>
<span data-ttu-id="645db-119">W tym przykładzie wszystkie poświadczenia zostaną usunięte z aplikacji skojarzonej z identyfikatorem Skype "4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58".</span><span class="sxs-lookup"><span data-stu-id="645db-119">In this example, all credentials will be removed from the application associated with the applicationId "4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58".</span></span>

## <span data-ttu-id="645db-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="645db-120">PARAMETERS</span></span>

### <span data-ttu-id="645db-121">-All</span><span class="sxs-lookup"><span data-stu-id="645db-121">-All</span></span>
<span data-ttu-id="645db-122">Przełącz, aby usunąć wszystkie poświadczenia skojarzone z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="645db-122">Switch to remove all the credentials associated with the application.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ApplicationObjectIdWithAllParameterSet, ApplicationIdWithAllParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="645db-123">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="645db-123">-ApplicationId</span></span>
<span data-ttu-id="645db-124">Identyfikator aplikacji, z której mają zostać usunięte poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="645db-124">The id of the application to remove the credentials from.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationIdWithKeyIdParameterSet, ApplicationIdWithAllParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="645db-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="645db-125">-DefaultProfile</span></span>
<span data-ttu-id="645db-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="645db-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="645db-127">-Force</span><span class="sxs-lookup"><span data-stu-id="645db-127">-Force</span></span>
<span data-ttu-id="645db-128">Przełączanie do usuwania poświadczenia bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="645db-128">Switch to delete credential without a confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="645db-129">-KeyId</span><span class="sxs-lookup"><span data-stu-id="645db-129">-KeyId</span></span>
<span data-ttu-id="645db-130">Określa klucz poświadczenia, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="645db-130">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="645db-131">Identyfikatory kluczy aplikacji można uzyskać przy użyciu polecenia cmdlet Get-AzureRmADAppCredential.</span><span class="sxs-lookup"><span data-stu-id="645db-131">The key Ids for the application can be obtained using the Get-AzureRmADAppCredential cmdlet.</span></span>

```yaml
Type: Guid
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet, ApplicationIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="645db-132">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="645db-132">-ObjectId</span></span>
<span data-ttu-id="645db-133">Identyfikator obiektu aplikacji, z którego mają zostać usunięte poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="645db-133">The object id of the application to remove the credentials from.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet, ApplicationObjectIdWithAllParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="645db-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="645db-134">-Confirm</span></span>
<span data-ttu-id="645db-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="645db-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="645db-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="645db-136">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="645db-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="645db-137">CommonParameters</span></span>
<span data-ttu-id="645db-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="645db-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="645db-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="645db-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="645db-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="645db-140">INPUTS</span></span>

### <span data-ttu-id="645db-141">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="645db-141">None</span></span>
<span data-ttu-id="645db-142">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="645db-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="645db-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="645db-143">OUTPUTS</span></span>

## <span data-ttu-id="645db-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="645db-144">NOTES</span></span>

## <span data-ttu-id="645db-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="645db-145">RELATED LINKS</span></span>

[<span data-ttu-id="645db-146">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="645db-146">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="645db-147">Nowe — AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="645db-147">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="645db-148">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="645db-148">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)
