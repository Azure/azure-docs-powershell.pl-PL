---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 04B1E3A6-6D52-46A3-8241-2CCDB5E71642
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADSpCredential.md
ms.openlocfilehash: b1f4b8d53a1031cef76d51a87bbf9afa5b75758f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718717"
---
# <span data-ttu-id="a2079-101">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="a2079-101">Remove-AzureRmADSpCredential</span></span>

## <span data-ttu-id="a2079-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a2079-102">SYNOPSIS</span></span>
<span data-ttu-id="a2079-103">Usuwa poświadczenia z podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="a2079-103">Removes a credential from a service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2079-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a2079-104">SYNTAX</span></span>

### <span data-ttu-id="a2079-105">ObjectIdWithKeyIdParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a2079-105">ObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzureRmADSpCredential -ObjectId <String> -KeyId <Guid> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2079-106">ObjectIdWithAllParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2079-106">ObjectIdWithAllParameterSet</span></span>
```
Remove-AzureRmADSpCredential -ObjectId <String> [-All] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2079-107">SPNWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2079-107">SPNWithKeyIdParameterSet</span></span>
```
Remove-AzureRmADSpCredential -ServicePrincipalName <String> -KeyId <Guid> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2079-108">SPNWithAllParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2079-108">SPNWithAllParameterSet</span></span>
```
Remove-AzureRmADSpCredential -ServicePrincipalName <String> [-All] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2079-109">Opis</span><span class="sxs-lookup"><span data-stu-id="a2079-109">DESCRIPTION</span></span>
<span data-ttu-id="a2079-110">Polecenia cmdlet Remove-AzureRmADSpCredential można użyć w celu usunięcia klucza poświadczeń z podmiotu zabezpieczeń usługi w przypadku złamania zabezpieczeń lub jako część wygaśnięcia przerzucania klucza poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="a2079-110">The Remove-AzureRmADSpCredential cmdlet can be used to remove a credential key from a service principal in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="a2079-111">Wartość główna usługi jest identyfikowana przez podanie identyfikatora obiektu lub głównej nazwy usługi (SPN).</span><span class="sxs-lookup"><span data-stu-id="a2079-111">The service principal is identified by supplying either the object ID or service principal name (SPN).</span></span>

<span data-ttu-id="a2079-112">Poświadczenie, które ma zostać usunięte, jest identyfikowane przez identyfikator klucza, jeśli pojedyncze poświadczenie ma zostać usunięte lub z przełącznikiem wszystkie, aby usunąć wszystkie poświadczenia skojarzone z podmiotem zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="a2079-112">The credential to be removed is identified by its key ID if an individual credential is to be removed or with an 'All' switch to delete all credentials associated with the service principal.</span></span>

## <span data-ttu-id="a2079-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a2079-113">EXAMPLES</span></span>

### <span data-ttu-id="a2079-114">--------------------------Przykład 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a2079-114">--------------------------  Example 1  --------------------------</span></span>
```
PS E:\> Remove-AzureRmADSpCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="a2079-115">To polecenie usuwa klucz poświadczenia z podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="a2079-115">This command removes a credential key from a service principal.</span></span>
<span data-ttu-id="a2079-116">W tym przykładzie klucz z identyfikatorem "9044423a-60a3-45ac-9ab1-09534157ebb" zostanie usunięty z podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="a2079-116">In this example, the key with Id "9044423a-60a3-45ac-9ab1-09534157ebb" will be removed from the service principal.</span></span>

### <span data-ttu-id="a2079-117">--------------------------Przykład 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="a2079-117">--------------------------  Example 2  --------------------------</span></span>
```
PS E:\> Remove-AzureRmADSpCredential -ServicePrincipalName http://test123 -All
```

<span data-ttu-id="a2079-118">To polecenie usuwa klucz poświadczenia z podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="a2079-118">This command removes a credential key from a service principal.</span></span>
<span data-ttu-id="a2079-119">W tym przykładzie wszystkie poświadczenia zostaną usunięte z podmiotu zabezpieczeń usługi skojarzonego z główną nazwą usługi " http://test123 ".</span><span class="sxs-lookup"><span data-stu-id="a2079-119">In this example, all credentials will be removed from the service principal associated with the service principal name "http://test123".</span></span>

## <span data-ttu-id="a2079-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a2079-120">PARAMETERS</span></span>

### <span data-ttu-id="a2079-121">-All</span><span class="sxs-lookup"><span data-stu-id="a2079-121">-All</span></span>
<span data-ttu-id="a2079-122">Przełącz, aby usunąć wszystkie poświadczenia skojarzone z podmiotem zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="a2079-122">Switch to remove all the credentials associated with the service principal.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ObjectIdWithAllParameterSet, SPNWithAllParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2079-123">-Force</span><span class="sxs-lookup"><span data-stu-id="a2079-123">-Force</span></span>
<span data-ttu-id="a2079-124">Przełączanie do usuwania poświadczenia bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="a2079-124">Switch to delete credential without a confirmation.</span></span>

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

### <span data-ttu-id="a2079-125">-KeyId</span><span class="sxs-lookup"><span data-stu-id="a2079-125">-KeyId</span></span>
<span data-ttu-id="a2079-126">Określa klucz poświadczenia, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="a2079-126">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="a2079-127">Identyfikatory kluczy dla podmiotu usługi można uzyskać przy użyciu polecenia cmdlet Get-AzureRmADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="a2079-127">The key Ids for a service principal can be obtained using the Get-AzureRmADSpCredential cmdlet.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdWithKeyIdParameterSet, SPNWithKeyIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2079-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="a2079-128">-ObjectId</span></span>
<span data-ttu-id="a2079-129">Identyfikator obiektu podmiotu usługi, z którego mają zostać usunięte poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="a2079-129">The object id of the service principal to remove the credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdWithKeyIdParameterSet, ObjectIdWithAllParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2079-130">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="a2079-130">-ServicePrincipalName</span></span>
<span data-ttu-id="a2079-131">Nazwa (SPN) podmiotu usługi, z którego mają zostać usunięte poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="a2079-131">The name (SPN) of the service principal to remove the credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNWithKeyIdParameterSet, SPNWithAllParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2079-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a2079-132">-Confirm</span></span>
<span data-ttu-id="a2079-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2079-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2079-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2079-134">-WhatIf</span></span>
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

### <span data-ttu-id="a2079-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2079-135">-DefaultProfile</span></span>
<span data-ttu-id="a2079-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a2079-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2079-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2079-137">CommonParameters</span></span>
<span data-ttu-id="a2079-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2079-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2079-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2079-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2079-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a2079-140">INPUTS</span></span>

## <span data-ttu-id="a2079-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a2079-141">OUTPUTS</span></span>

## <span data-ttu-id="a2079-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a2079-142">NOTES</span></span>

## <span data-ttu-id="a2079-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a2079-143">RELATED LINKS</span></span>

[<span data-ttu-id="a2079-144">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="a2079-144">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

[<span data-ttu-id="a2079-145">Nowe — AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="a2079-145">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="a2079-146">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="a2079-146">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

