---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6AC9DA05-756D-4D59-BD97-DBAAFBB3C7AC
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADAppCredential.md
ms.openlocfilehash: c96fceb331a2b33528b47506e928ea78cfc793d1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974474"
---
# <span data-ttu-id="181aa-101">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="181aa-101">Get-AzADAppCredential</span></span>

## <span data-ttu-id="181aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="181aa-102">SYNOPSIS</span></span>
<span data-ttu-id="181aa-103">Pobiera listę poświadczeń skojarzonych z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="181aa-103">Retrieves a list of credentials associated with an application.</span></span>

## <span data-ttu-id="181aa-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="181aa-104">SYNTAX</span></span>

### <span data-ttu-id="181aa-105">ApplicationObjectIdParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="181aa-105">ApplicationObjectIdParameterSet (Default)</span></span>
```
Get-AzADAppCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="181aa-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="181aa-106">ApplicationIdParameterSet</span></span>
```
Get-AzADAppCredential -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="181aa-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="181aa-107">DisplayNameParameterSet</span></span>
```
Get-AzADAppCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="181aa-108">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="181aa-108">ApplicationObjectParameterSet</span></span>
```
Get-AzADAppCredential -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="181aa-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="181aa-109">DESCRIPTION</span></span>
<span data-ttu-id="181aa-110">To Get-AzADAppCredential cmdlet umożliwia pobranie listy poświadczeń skojarzonych z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="181aa-110">The Get-AzADAppCredential cmdlet can be used to retrieve a list of credentials associated with an application.</span></span>
<span data-ttu-id="181aa-111">To polecenie spowoduje pobranie wszystkich właściwości poświadczeń (ale nie wartości poświadczeń) skojarzonych z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="181aa-111">This command will retrieve all of the credential properties (but not the credential value) associated with the application.</span></span>

## <span data-ttu-id="181aa-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="181aa-112">EXAMPLES</span></span>

### <span data-ttu-id="181aa-113">Przykład 1. Uzyskiwanie poświadczeń aplikacji według identyfikatora obiektu</span><span class="sxs-lookup"><span data-stu-id="181aa-113">Example 1: Get application credentials by object id</span></span>

```powershell
PS C:\> Get-AzADAppCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
```

<span data-ttu-id="181aa-114">Zwraca listę poświadczeń skojarzonych z aplikacją o identyfikatorze obiektu '1f99cf81-0146-4f4e-beae-2007d0668476'.</span><span class="sxs-lookup"><span data-stu-id="181aa-114">Returns a list of credentials associated with the application having object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

### <span data-ttu-id="181aa-115">Przykład 2. Uzyskiwanie poświadczeń aplikacji za pomocą rur</span><span class="sxs-lookup"><span data-stu-id="181aa-115">Example 2: Get application credentials by piping</span></span>

```powershell
PS C:\> Get-AzADApplication -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | Get-AzADAppCredential
```

<span data-ttu-id="181aa-116">Pobiera aplikację o identyfikatorze obiektu "1f99cf81-0146-4f4e-beae-2007d0668476" i potokuje ją do polecenia cmdlet programu Get-AzADAppCredential w celu podania listy wszystkich poświadczeń dla tej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="181aa-116">Gets the application with object id '1f99cf81-0146-4f4e-beae-2007d0668476' and pipes it to the Get-AzADAppCredential cmdlet to list all of the credentials for that application.</span></span>

## <span data-ttu-id="181aa-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="181aa-117">PARAMETERS</span></span>

### <span data-ttu-id="181aa-118">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="181aa-118">-ApplicationId</span></span>
<span data-ttu-id="181aa-119">Identyfikator aplikacji, z których mają być pobierane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="181aa-119">The id of the application to retrieve credentials from.</span></span>

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

### <span data-ttu-id="181aa-120">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="181aa-120">-ApplicationObject</span></span>
<span data-ttu-id="181aa-121">Obiekt aplikacji, z który mają być pobierane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="181aa-121">The application object to retrieve credentials from.</span></span>

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

### <span data-ttu-id="181aa-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="181aa-122">-DefaultProfile</span></span>
<span data-ttu-id="181aa-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="181aa-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="181aa-124">— DisplayName</span><span class="sxs-lookup"><span data-stu-id="181aa-124">-DisplayName</span></span>
<span data-ttu-id="181aa-125">Nazwa wyświetlana aplikacji.</span><span class="sxs-lookup"><span data-stu-id="181aa-125">The display name of the application.</span></span>

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

### <span data-ttu-id="181aa-126">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="181aa-126">-ObjectId</span></span>
<span data-ttu-id="181aa-127">Identyfikator obiektu aplikacji, z których mają być pobierane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="181aa-127">The object id of the application to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="181aa-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="181aa-128">CommonParameters</span></span>
<span data-ttu-id="181aa-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="181aa-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="181aa-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="181aa-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="181aa-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="181aa-131">INPUTS</span></span>

### <span data-ttu-id="181aa-132">System.String</span><span class="sxs-lookup"><span data-stu-id="181aa-132">System.String</span></span>

### <span data-ttu-id="181aa-133">System.Guid</span><span class="sxs-lookup"><span data-stu-id="181aa-133">System.Guid</span></span>

### <span data-ttu-id="181aa-134">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="181aa-134">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="181aa-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="181aa-135">OUTPUTS</span></span>

### <span data-ttu-id="181aa-136">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span><span class="sxs-lookup"><span data-stu-id="181aa-136">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="181aa-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="181aa-137">NOTES</span></span>

## <span data-ttu-id="181aa-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="181aa-138">RELATED LINKS</span></span>

[<span data-ttu-id="181aa-139">New-AzadAppCredential</span><span class="sxs-lookup"><span data-stu-id="181aa-139">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="181aa-140">Remove-AzadAppCredential</span><span class="sxs-lookup"><span data-stu-id="181aa-140">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="181aa-141">Get-AzadApplication</span><span class="sxs-lookup"><span data-stu-id="181aa-141">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

