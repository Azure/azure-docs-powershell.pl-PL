---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C61FA834-BEBE-4DBF-888F-C6CB8CC95390
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADAppCredential.md
ms.openlocfilehash: a5e99f045701a373e14990c25627696d40a04a37
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549875"
---
# <span data-ttu-id="890d3-101">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="890d3-101">Remove-AzureRmADAppCredential</span></span>

## <span data-ttu-id="890d3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="890d3-102">SYNOPSIS</span></span>
<span data-ttu-id="890d3-103">Usuwa poświadczenie z aplikacji.</span><span class="sxs-lookup"><span data-stu-id="890d3-103">Removes a credential from an application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="890d3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="890d3-104">SYNTAX</span></span>

### <span data-ttu-id="890d3-105">ApplicationObjectIdWithKeyIdParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="890d3-105">ApplicationObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzureRmADAppCredential -ObjectId <String> -KeyId <Guid> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="890d3-106">ApplicationObjectIdWithAllParameterSet</span><span class="sxs-lookup"><span data-stu-id="890d3-106">ApplicationObjectIdWithAllParameterSet</span></span>
```
Remove-AzureRmADAppCredential -ObjectId <String> [-All] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="890d3-107">ApplicationIdWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="890d3-107">ApplicationIdWithKeyIdParameterSet</span></span>
```
Remove-AzureRmADAppCredential -ApplicationId <String> -KeyId <Guid> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="890d3-108">ApplicationIdWithAllParameterSet</span><span class="sxs-lookup"><span data-stu-id="890d3-108">ApplicationIdWithAllParameterSet</span></span>
```
Remove-AzureRmADAppCredential -ApplicationId <String> [-All] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="890d3-109">Opis</span><span class="sxs-lookup"><span data-stu-id="890d3-109">DESCRIPTION</span></span>
<span data-ttu-id="890d3-110">Polecenia cmdlet Remove-AzureRmADAppCredential można użyć w celu usunięcia klucza poświadczeń z aplikacji w przypadku złamania zabezpieczeń lub w ramach wygaśnięcia klucza poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="890d3-110">The Remove-AzureRmADAppCredential cmdlet can be used to remove a credential key from an application in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="890d3-111">Aplikacja jest identyfikowana przez podanie identyfikatora obiektu lub identyfikatora aplikacji.</span><span class="sxs-lookup"><span data-stu-id="890d3-111">The application is identified by supplying either the object ID or AppId.</span></span>
<span data-ttu-id="890d3-112">Poświadczenie, które ma zostać usunięte, jest identyfikowane za pomocą identyfikatora klucza, jeśli pojedyncze poświadczenie zostanie usunięte lub z przełącznikiem wszystkie, w celu usunięcia wszystkich poświadczeń skojarzonych z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="890d3-112">The credential to be removed is identified by its key ID if an individual credential is to be removed or with an 'All' switch to delete all credentials associated with the application.</span></span>

## <span data-ttu-id="890d3-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="890d3-113">EXAMPLES</span></span>

### <span data-ttu-id="890d3-114">--------------------------Przykład 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="890d3-114">--------------------------  Example 1  --------------------------</span></span>
```
PS E:\> Remove-AzureRmADAppCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="890d3-115">To polecenie usuwa klucz poświadczenia z aplikacji.</span><span class="sxs-lookup"><span data-stu-id="890d3-115">This command removes a credential key from an application.</span></span>
<span data-ttu-id="890d3-116">W tym przykładzie klucz z identyfikatorem "9044423a-60a3-45ac-9ab1-09534157ebb" zostanie usunięty z aplikacji.</span><span class="sxs-lookup"><span data-stu-id="890d3-116">In this example, the key with Id "9044423a-60a3-45ac-9ab1-09534157ebb" will be removed from the application.</span></span>

### <span data-ttu-id="890d3-117">--------------------------Przykład 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="890d3-117">--------------------------  Example 2  --------------------------</span></span>
```
PS E:\> Remove-AzureRmADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 -All
```

<span data-ttu-id="890d3-118">To polecenie usuwa klucz poświadczenia z aplikacji.</span><span class="sxs-lookup"><span data-stu-id="890d3-118">This command removes a credential key from an application.</span></span>
<span data-ttu-id="890d3-119">W tym przykładzie wszystkie poświadczenia zostaną usunięte z aplikacji skojarzonej z identyfikatorem Skype "4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58".</span><span class="sxs-lookup"><span data-stu-id="890d3-119">In this example, all credentials will be removed from the application associated with the applicationId "4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58".</span></span>

## <span data-ttu-id="890d3-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="890d3-120">PARAMETERS</span></span>

### <span data-ttu-id="890d3-121">-All</span><span class="sxs-lookup"><span data-stu-id="890d3-121">-All</span></span>
<span data-ttu-id="890d3-122">Przełącz, aby usunąć wszystkie poświadczenia skojarzone z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="890d3-122">Switch to remove all the credentials associated with the application.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ApplicationObjectIdWithAllParameterSet, ApplicationIdWithAllParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="890d3-123">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="890d3-123">-ApplicationId</span></span>
<span data-ttu-id="890d3-124">Identyfikator aplikacji, z której mają zostać usunięte poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="890d3-124">The id of the application to remove the credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationIdWithKeyIdParameterSet, ApplicationIdWithAllParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="890d3-125">-Force</span><span class="sxs-lookup"><span data-stu-id="890d3-125">-Force</span></span>
<span data-ttu-id="890d3-126">Przełączanie do usuwania poświadczenia bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="890d3-126">Switch to delete credential without a confirmation.</span></span>

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

### <span data-ttu-id="890d3-127">-KeyId</span><span class="sxs-lookup"><span data-stu-id="890d3-127">-KeyId</span></span>
<span data-ttu-id="890d3-128">Określa klucz poświadczenia, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="890d3-128">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="890d3-129">Identyfikatory kluczy aplikacji można uzyskać przy użyciu polecenia cmdlet Get-AzureRmADAppCredential.</span><span class="sxs-lookup"><span data-stu-id="890d3-129">The key Ids for the application can be obtained using the Get-AzureRmADAppCredential cmdlet.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet, ApplicationIdWithKeyIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="890d3-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="890d3-130">-ObjectId</span></span>
<span data-ttu-id="890d3-131">Identyfikator obiektu aplikacji, z którego mają zostać usunięte poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="890d3-131">The object id of the application to remove the credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet, ApplicationObjectIdWithAllParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="890d3-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="890d3-132">-Confirm</span></span>
<span data-ttu-id="890d3-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="890d3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="890d3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="890d3-134">-WhatIf</span></span>
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

### <span data-ttu-id="890d3-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="890d3-135">-DefaultProfile</span></span>
<span data-ttu-id="890d3-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="890d3-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="890d3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="890d3-137">CommonParameters</span></span>
<span data-ttu-id="890d3-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="890d3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="890d3-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="890d3-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="890d3-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="890d3-140">INPUTS</span></span>

## <span data-ttu-id="890d3-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="890d3-141">OUTPUTS</span></span>

## <span data-ttu-id="890d3-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="890d3-142">NOTES</span></span>

## <span data-ttu-id="890d3-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="890d3-143">RELATED LINKS</span></span>

[<span data-ttu-id="890d3-144">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="890d3-144">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="890d3-145">Nowe — AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="890d3-145">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="890d3-146">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="890d3-146">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)
