---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6AC9DA05-756D-4D59-BD97-DBAAFBB3C7AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADAppCredential.md
ms.openlocfilehash: 7bfa908e83d7731ca2ed5613d82f42b19c392b2f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178914"
---
# <span data-ttu-id="05c43-101">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="05c43-101">Get-AzADAppCredential</span></span>

## <span data-ttu-id="05c43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05c43-102">SYNOPSIS</span></span>
<span data-ttu-id="05c43-103">Pobiera listę poświadczeń skojarzonych z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="05c43-103">Retrieves a list of credentials associated with an application.</span></span>

## <span data-ttu-id="05c43-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="05c43-104">SYNTAX</span></span>

### <span data-ttu-id="05c43-105">ApplicationObjectIdParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="05c43-105">ApplicationObjectIdParameterSet (Default)</span></span>
```
Get-AzADAppCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05c43-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="05c43-106">ApplicationIdParameterSet</span></span>
```
Get-AzADAppCredential -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05c43-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="05c43-107">DisplayNameParameterSet</span></span>
```
Get-AzADAppCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05c43-108">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="05c43-108">ApplicationObjectParameterSet</span></span>
```
Get-AzADAppCredential -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="05c43-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="05c43-109">DESCRIPTION</span></span>
<span data-ttu-id="05c43-110">Za Get-AzADAppCredential cmdlet można pobrać listę poświadczeń skojarzonych z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="05c43-110">The Get-AzADAppCredential cmdlet can be used to retrieve a list of credentials associated with an application.</span></span>
<span data-ttu-id="05c43-111">To polecenie spowoduje pobranie wszystkich właściwości poświadczeń (ale nie wartości poświadczeń) skojarzonych z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="05c43-111">This command will retrieve all of the credential properties (but not the credential value) associated with the application.</span></span>

## <span data-ttu-id="05c43-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="05c43-112">EXAMPLES</span></span>

### <span data-ttu-id="05c43-113">Przykład 1. Uzyskiwanie poświadczeń aplikacji według identyfikatora obiektu</span><span class="sxs-lookup"><span data-stu-id="05c43-113">Example 1: Get application credentials by object id</span></span>

```powershell
PS C:\> Get-AzADAppCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
```

<span data-ttu-id="05c43-114">Zwraca listę poświadczeń skojarzonych z aplikacją o identyfikatorze obiektu '1f99cf81-0146-4f4e-beae-2007d0668476'.</span><span class="sxs-lookup"><span data-stu-id="05c43-114">Returns a list of credentials associated with the application having object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

### <span data-ttu-id="05c43-115">Przykład 2. Uzyskiwanie poświadczeń aplikacji za pomocą rur</span><span class="sxs-lookup"><span data-stu-id="05c43-115">Example 2: Get application credentials by piping</span></span>

```powershell
PS C:\> Get-AzADApplication -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | Get-AzADAppCredential
```

<span data-ttu-id="05c43-116">Pobiera aplikację z identyfikatorem obiektu "1f99cf81-0146-4f4e-beae-2007d0668476" i potokuje ją do polecenia cmdlet programu Get-AzADAppCredential w celu podania listy wszystkich poświadczeń dla tej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="05c43-116">Gets the application with object id '1f99cf81-0146-4f4e-beae-2007d0668476' and pipes it to the Get-AzADAppCredential cmdlet to list all of the credentials for that application.</span></span>

## <span data-ttu-id="05c43-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="05c43-117">PARAMETERS</span></span>

### <span data-ttu-id="05c43-118">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="05c43-118">-ApplicationId</span></span>
<span data-ttu-id="05c43-119">Identyfikator aplikacji, z których mają być pobierane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="05c43-119">The id of the application to retrieve credentials from.</span></span>

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

### <span data-ttu-id="05c43-120">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="05c43-120">-ApplicationObject</span></span>
<span data-ttu-id="05c43-121">Obiekt aplikacji, z który mają być pobierane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="05c43-121">The application object to retrieve credentials from.</span></span>

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

### <span data-ttu-id="05c43-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05c43-122">-DefaultProfile</span></span>
<span data-ttu-id="05c43-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="05c43-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="05c43-124">— DisplayName</span><span class="sxs-lookup"><span data-stu-id="05c43-124">-DisplayName</span></span>
<span data-ttu-id="05c43-125">Nazwa wyświetlana aplikacji.</span><span class="sxs-lookup"><span data-stu-id="05c43-125">The display name of the application.</span></span>

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

### <span data-ttu-id="05c43-126">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="05c43-126">-ObjectId</span></span>
<span data-ttu-id="05c43-127">Identyfikator obiektu aplikacji, z których mają być pobierane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="05c43-127">The object id of the application to retrieve credentials from.</span></span>

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

### <span data-ttu-id="05c43-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05c43-128">CommonParameters</span></span>
<span data-ttu-id="05c43-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05c43-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05c43-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="05c43-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05c43-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="05c43-131">INPUTS</span></span>

### <span data-ttu-id="05c43-132">System.String</span><span class="sxs-lookup"><span data-stu-id="05c43-132">System.String</span></span>

### <span data-ttu-id="05c43-133">System.Guid</span><span class="sxs-lookup"><span data-stu-id="05c43-133">System.Guid</span></span>

### <span data-ttu-id="05c43-134">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="05c43-134">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="05c43-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="05c43-135">OUTPUTS</span></span>

### <span data-ttu-id="05c43-136">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span><span class="sxs-lookup"><span data-stu-id="05c43-136">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="05c43-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="05c43-137">NOTES</span></span>

## <span data-ttu-id="05c43-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="05c43-138">RELATED LINKS</span></span>

[<span data-ttu-id="05c43-139">New-AzadAppCredential</span><span class="sxs-lookup"><span data-stu-id="05c43-139">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="05c43-140">Remove-AzadAppCredential</span><span class="sxs-lookup"><span data-stu-id="05c43-140">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="05c43-141">Get-AzadApplication</span><span class="sxs-lookup"><span data-stu-id="05c43-141">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

