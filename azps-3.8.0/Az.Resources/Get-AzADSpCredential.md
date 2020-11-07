---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 7690143F-5F09-4739-9F66-B2ACDF8305F4
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADSpCredential.md
ms.openlocfilehash: c22643c4ce47fc59d2640a6dbbdf9c15b0846f98
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93895965"
---
# <span data-ttu-id="4805f-101">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="4805f-101">Get-AzADSpCredential</span></span>

## <span data-ttu-id="4805f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4805f-102">SYNOPSIS</span></span>
<span data-ttu-id="4805f-103">Pobiera listę poświadczeń skojarzonych z podmiotem zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="4805f-103">Retrieves a list of credentials associated with a service principal.</span></span>

## <span data-ttu-id="4805f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4805f-104">SYNTAX</span></span>

### <span data-ttu-id="4805f-105">ObjectIdParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4805f-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzADSpCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4805f-106">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="4805f-106">SPNParameterSet</span></span>
```
Get-AzADSpCredential -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4805f-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4805f-107">DisplayNameParameterSet</span></span>
```
Get-AzADSpCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4805f-108">SPNObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4805f-108">SPNObjectParameterSet</span></span>
```
Get-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4805f-109">Opis</span><span class="sxs-lookup"><span data-stu-id="4805f-109">DESCRIPTION</span></span>
<span data-ttu-id="4805f-110">Polecenie cmdlet Get-AzADSpCredential może służyć do pobierania listy poświadczeń skojarzonych z podmiotem zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="4805f-110">The Get-AzADSpCredential cmdlet can be used to retrieve a list of credentials associated with a service principal.</span></span>
<span data-ttu-id="4805f-111">To polecenie spowoduje pobranie wszystkich właściwości poświadczeń (ale nie wartości poświadczeń) skojarzonych z podmiotem zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="4805f-111">This command will retrieve all of the credential properties (but not the credential value) associated with the service principal.</span></span>

## <span data-ttu-id="4805f-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4805f-112">EXAMPLES</span></span>

### <span data-ttu-id="4805f-113">Przykład 1-listowe poświadczenia według nazwy SPN</span><span class="sxs-lookup"><span data-stu-id="4805f-113">Example 1 - List credentials by SPN</span></span>

```
PS C:\> Get-AzADSpCredential -ServicePrincipalName http://test12345
```

<span data-ttu-id="4805f-114">Zwraca listę poświadczeń skojarzonych z podmiotem zabezpieczeń usługi z główną wersją SPN http://test12345 .</span><span class="sxs-lookup"><span data-stu-id="4805f-114">Returns a list of credentials associated with the service principal with SPN 'http://test12345'.</span></span>

### <span data-ttu-id="4805f-115">Przykład 2-Wyświetlanie listy poświadczeń według identyfikatora obiektu</span><span class="sxs-lookup"><span data-stu-id="4805f-115">Example 2 - List credentials by object id</span></span>

```
PS C:\> Get-AzADSpCredential -ObjectId 58e28616-99cc-4da4-b705-7672130e1047
```

<span data-ttu-id="4805f-116">Zwraca listę poświadczeń skojarzonych z podmiotem zabezpieczeń usługi o identyfikatorze obiektu "58e28616-99cc-4da4-b705-7672130e1047".</span><span class="sxs-lookup"><span data-stu-id="4805f-116">Returns a list of credentials associated with the service principal with object id "58e28616-99cc-4da4-b705-7672130e1047".</span></span>

### <span data-ttu-id="4805f-117">Przykład 3-Wyświetlaj poświadczenia według połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="4805f-117">Example 3 - List credentials by piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 58e28616-99cc-4da4-b705-7672130e1047 | Get-AzADSpCredential
```

<span data-ttu-id="4805f-118">Pobiera podmiot zabezpieczeń usługi o identyfikatorze obiektu "58e28616-99cc-4da4-b705-7672130e1047" i przekazuje go do polecenia cmdlet Get-AzADSpCredential, aby wyświetlić wszystkie poświadczenia dla tego podmiotu usługi.</span><span class="sxs-lookup"><span data-stu-id="4805f-118">Gets the service principal with object id "58e28616-99cc-4da4-b705-7672130e1047" and pipes it to the Get-AzADSpCredential cmdlet to list all credentials for that service principal.</span></span>

## <span data-ttu-id="4805f-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4805f-119">PARAMETERS</span></span>

### <span data-ttu-id="4805f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4805f-120">-DefaultProfile</span></span>
<span data-ttu-id="4805f-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="4805f-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4805f-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="4805f-122">-DisplayName</span></span>
<span data-ttu-id="4805f-123">Nazwa wyświetlana podmiotu zabezpieczeń usługi</span><span class="sxs-lookup"><span data-stu-id="4805f-123">The display name of the service principal</span></span>

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

### <span data-ttu-id="4805f-124">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="4805f-124">-ObjectId</span></span>
<span data-ttu-id="4805f-125">Identyfikator obiektu podmiotu usługi, z którego mają być pobierane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="4805f-125">The object id of the service principal to retrieve credentials from.</span></span>

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

### <span data-ttu-id="4805f-126">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="4805f-126">-ServicePrincipalName</span></span>
<span data-ttu-id="4805f-127">Nazwa (SPN) podmiotu zabezpieczeń usługi, z którego mają być pobierane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="4805f-127">The name (SPN) of the service principal to retrieve credentials from.</span></span>

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

### <span data-ttu-id="4805f-128">-Serviceprincipalobject</span><span class="sxs-lookup"><span data-stu-id="4805f-128">-ServicePrincipalObject</span></span>
<span data-ttu-id="4805f-129">Obiekt główny usługi, z którego mają zostać pobrane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="4805f-129">The service principal object to retrieve the credentials from.</span></span>

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

### <span data-ttu-id="4805f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4805f-130">CommonParameters</span></span>
<span data-ttu-id="4805f-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4805f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4805f-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4805f-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4805f-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4805f-133">INPUTS</span></span>

### <span data-ttu-id="4805f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="4805f-134">System.String</span></span>

### <span data-ttu-id="4805f-135">Microsoft. Azure. Commands. pozycji. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="4805f-135">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="4805f-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4805f-136">OUTPUTS</span></span>

### <span data-ttu-id="4805f-137">Microsoft. Azure. Commands. pozycji. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="4805f-137">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="4805f-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4805f-138">NOTES</span></span>

## <span data-ttu-id="4805f-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4805f-139">RELATED LINKS</span></span>

[<span data-ttu-id="4805f-140">Nowe — AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="4805f-140">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="4805f-141">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="4805f-141">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

[<span data-ttu-id="4805f-142">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="4805f-142">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

