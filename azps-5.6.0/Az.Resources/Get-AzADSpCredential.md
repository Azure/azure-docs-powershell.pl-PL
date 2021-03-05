---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 7690143F-5F09-4739-9F66-B2ACDF8305F4
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADSpCredential.md
ms.openlocfilehash: 83212224ba14e0a079db936d058522d4759430fd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961697"
---
# <span data-ttu-id="a0b8d-101">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="a0b8d-101">Get-AzADSpCredential</span></span>

## <span data-ttu-id="a0b8d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0b8d-102">SYNOPSIS</span></span>
<span data-ttu-id="a0b8d-103">Pobiera listę poświadczeń skojarzonych z podmiotem zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="a0b8d-103">Retrieves a list of credentials associated with a service principal.</span></span>

## <span data-ttu-id="a0b8d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a0b8d-104">SYNTAX</span></span>

### <span data-ttu-id="a0b8d-105">ObjectIdParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="a0b8d-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzADSpCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a0b8d-106">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0b8d-106">SPNParameterSet</span></span>
```
Get-AzADSpCredential -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a0b8d-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0b8d-107">DisplayNameParameterSet</span></span>
```
Get-AzADSpCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a0b8d-108">SPNObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0b8d-108">SPNObjectParameterSet</span></span>
```
Get-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a0b8d-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="a0b8d-109">DESCRIPTION</span></span>
<span data-ttu-id="a0b8d-110">Za Get-AzADSpCredential cmdlet można pobrać listę poświadczeń skojarzonych z podmiotem zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="a0b8d-110">The Get-AzADSpCredential cmdlet can be used to retrieve a list of credentials associated with a service principal.</span></span>
<span data-ttu-id="a0b8d-111">To polecenie spowoduje pobranie wszystkich właściwości poświadczeń (ale nie wartości poświadczeń) skojarzonych z podmiotem zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="a0b8d-111">This command will retrieve all of the credential properties (but not the credential value) associated with the service principal.</span></span>

## <span data-ttu-id="a0b8d-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a0b8d-112">EXAMPLES</span></span>

### <span data-ttu-id="a0b8d-113">Przykład 1. Poświadczenia listy według sieci SPN</span><span class="sxs-lookup"><span data-stu-id="a0b8d-113">Example 1 - List credentials by SPN</span></span>

```
PS C:\> Get-AzADSpCredential -ServicePrincipalName http://test12345
```

<span data-ttu-id="a0b8d-114">Zwraca listę poświadczeń skojarzonych z podmiotem zabezpieczeń usługi z dodatkiem SPN ' http://test12345 '.</span><span class="sxs-lookup"><span data-stu-id="a0b8d-114">Returns a list of credentials associated with the service principal with SPN 'http://test12345'.</span></span>

### <span data-ttu-id="a0b8d-115">Przykład 2. Poświadczenia listy według identyfikatora obiektu</span><span class="sxs-lookup"><span data-stu-id="a0b8d-115">Example 2 - List credentials by object id</span></span>

```
PS C:\> Get-AzADSpCredential -ObjectId 58e28616-99cc-4da4-b705-7672130e1047
```

<span data-ttu-id="a0b8d-116">Zwraca listę poświadczeń skojarzonych z podmiotem zabezpieczeń usługi o identyfikatorze obiektu "58e28616-99cc-4da4-b705-7672130e1047".</span><span class="sxs-lookup"><span data-stu-id="a0b8d-116">Returns a list of credentials associated with the service principal with object id "58e28616-99cc-4da4-b705-7672130e1047".</span></span>

### <span data-ttu-id="a0b8d-117">Przykład 3. Poświadczeń listy za pomocą rur</span><span class="sxs-lookup"><span data-stu-id="a0b8d-117">Example 3 - List credentials by piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 58e28616-99cc-4da4-b705-7672130e1047 | Get-AzADSpCredential
```

<span data-ttu-id="a0b8d-118">Pobiera podmiot zabezpieczeń usługi o identyfikatorze obiektu "58e28616-99cc-4da4-b705-7672130e1047" i potokuje go do polecenia cmdlet usługi Get-AzADSpCredential w celu wytyczania listy wszystkich poświadczeń tego podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="a0b8d-118">Gets the service principal with object id "58e28616-99cc-4da4-b705-7672130e1047" and pipes it to the Get-AzADSpCredential cmdlet to list all credentials for that service principal.</span></span>

## <span data-ttu-id="a0b8d-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a0b8d-119">PARAMETERS</span></span>

### <span data-ttu-id="a0b8d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0b8d-120">-DefaultProfile</span></span>
<span data-ttu-id="a0b8d-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="a0b8d-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a0b8d-122">— DisplayName</span><span class="sxs-lookup"><span data-stu-id="a0b8d-122">-DisplayName</span></span>
<span data-ttu-id="a0b8d-123">Nazwa wyświetlana podmiotu zabezpieczeń usługi</span><span class="sxs-lookup"><span data-stu-id="a0b8d-123">The display name of the service principal</span></span>

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

### <span data-ttu-id="a0b8d-124">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="a0b8d-124">-ObjectId</span></span>
<span data-ttu-id="a0b8d-125">Identyfikator obiektu podmiotu zabezpieczeń usługi do pobierania poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="a0b8d-125">The object id of the service principal to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0b8d-126">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="a0b8d-126">-ServicePrincipalName</span></span>
<span data-ttu-id="a0b8d-127">Nazwa (SPN) podmiotu zabezpieczeń usługi, od których mają być pobierane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="a0b8d-127">The name (SPN) of the service principal to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0b8d-128">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="a0b8d-128">-ServicePrincipalObject</span></span>
<span data-ttu-id="a0b8d-129">Obiekt podmiotu zabezpieczeń usługi, z który mają być pobierane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="a0b8d-129">The service principal object to retrieve the credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: SPNObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a0b8d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0b8d-130">CommonParameters</span></span>
<span data-ttu-id="a0b8d-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0b8d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0b8d-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a0b8d-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0b8d-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a0b8d-133">INPUTS</span></span>

### <span data-ttu-id="a0b8d-134">System.String</span><span class="sxs-lookup"><span data-stu-id="a0b8d-134">System.String</span></span>

### <span data-ttu-id="a0b8d-135">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="a0b8d-135">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="a0b8d-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a0b8d-136">OUTPUTS</span></span>

### <span data-ttu-id="a0b8d-137">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span><span class="sxs-lookup"><span data-stu-id="a0b8d-137">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="a0b8d-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a0b8d-138">NOTES</span></span>

## <span data-ttu-id="a0b8d-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a0b8d-139">RELATED LINKS</span></span>

[<span data-ttu-id="a0b8d-140">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="a0b8d-140">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="a0b8d-141">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="a0b8d-141">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

[<span data-ttu-id="a0b8d-142">Get-AzadServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="a0b8d-142">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

