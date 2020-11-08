---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 7CB42968-8F6F-4D84-9AE2-1000F280BF3C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 586abbd5f203ce00f6faa7975d9e2adbd0c7940e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055515"
---
# <span data-ttu-id="f19b3-101">Get-AzureStorSimpleResourceContext</span><span class="sxs-lookup"><span data-stu-id="f19b3-101">Get-AzureStorSimpleResourceContext</span></span>

## <span data-ttu-id="f19b3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f19b3-102">SYNOPSIS</span></span>
<span data-ttu-id="f19b3-103">Pobiera bieżący kontekst zasobów.</span><span class="sxs-lookup"><span data-stu-id="f19b3-103">Gets the current resource context.</span></span>

## <span data-ttu-id="f19b3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f19b3-104">SYNTAX</span></span>

```
Get-AzureStorSimpleResourceContext [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f19b3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f19b3-105">DESCRIPTION</span></span>
<span data-ttu-id="f19b3-106">Polecenie cmdlet **Get-AzureStorSimpleResourceContext** Pobiera bieżący kontekst zasobów.</span><span class="sxs-lookup"><span data-stu-id="f19b3-106">The **Get-AzureStorSimpleResourceContext** cmdlet gets the current resource context.</span></span>

## <span data-ttu-id="f19b3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f19b3-107">EXAMPLES</span></span>

### <span data-ttu-id="f19b3-108">Przykład 1: uzyskiwanie bieżącego kontekstu</span><span class="sxs-lookup"><span data-stu-id="f19b3-108">Example 1: Get the current context</span></span>
```
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso63-Tsqa" 
PS C:\> Get-AzureStorSimpleResourceContext
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso63-Tsqa
```

<span data-ttu-id="f19b3-109">Pierwsze polecenie ustawia bieżący kontekst jako zasób o nazwie Contoso63-Tsqa przy użyciu polecenia cmdlet **SELECT-AzureStorSimpleResource** .</span><span class="sxs-lookup"><span data-stu-id="f19b3-109">The first command sets the current context to be the resource named Contoso63-Tsqa by using the **Select-AzureStorSimpleResource** cmdlet.</span></span>

<span data-ttu-id="f19b3-110">Drugie polecenie pobiera bieżący kontekst zasobów.</span><span class="sxs-lookup"><span data-stu-id="f19b3-110">The second command gets the current resource context.</span></span>

### <span data-ttu-id="f19b3-111">Przykład 2: próba pobrania bieżącego kontekstu</span><span class="sxs-lookup"><span data-stu-id="f19b3-111">Example 2: Attempt to get the current context</span></span>
```
PS C:\>Get-AzureStorSimpleResourceContext
Get-AzureStorSimpleResourceContext : Resource Context is not set for your subscription. Please use
Select-AzureStorSimpleResource -ResourceName <<name>> to set
```

<span data-ttu-id="f19b3-112">To polecenie pobiera bieżący kontekst.</span><span class="sxs-lookup"><span data-stu-id="f19b3-112">This command gets the current context.</span></span>
<span data-ttu-id="f19b3-113">W tym przykładzie nie ustawiono żadnego kontekstu.</span><span class="sxs-lookup"><span data-stu-id="f19b3-113">In this example, no context has been set.</span></span>
<span data-ttu-id="f19b3-114">Polecenie zwróci komunikat z wyjaśnieniem problemu.</span><span class="sxs-lookup"><span data-stu-id="f19b3-114">The command returns a message that explains the problem.</span></span>

## <span data-ttu-id="f19b3-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f19b3-115">PARAMETERS</span></span>

### <span data-ttu-id="f19b3-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="f19b3-116">-Profile</span></span>
<span data-ttu-id="f19b3-117">Określa Profil platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f19b3-117">Specifies an Azure profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f19b3-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f19b3-118">CommonParameters</span></span>
<span data-ttu-id="f19b3-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f19b3-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f19b3-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f19b3-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f19b3-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f19b3-121">INPUTS</span></span>

### <span data-ttu-id="f19b3-122">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="f19b3-122">None</span></span>

## <span data-ttu-id="f19b3-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f19b3-123">OUTPUTS</span></span>

### <span data-ttu-id="f19b3-124">StorSimpleResourceContext</span><span class="sxs-lookup"><span data-stu-id="f19b3-124">StorSimpleResourceContext</span></span>
<span data-ttu-id="f19b3-125">To polecenie cmdlet zwraca obiekt **ResourceContext** .</span><span class="sxs-lookup"><span data-stu-id="f19b3-125">This cmdlet returns a **ResourceContext** object.</span></span>

## <span data-ttu-id="f19b3-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f19b3-126">NOTES</span></span>

## <span data-ttu-id="f19b3-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f19b3-127">RELATED LINKS</span></span>

[<span data-ttu-id="f19b3-128">Get-AzureStorSimpleResource</span><span class="sxs-lookup"><span data-stu-id="f19b3-128">Get-AzureStorSimpleResource</span></span>](./Get-AzureStorSimpleResource.md)

[<span data-ttu-id="f19b3-129">Wybierz — AzureStorSimpleResource</span><span class="sxs-lookup"><span data-stu-id="f19b3-129">Select-AzureStorSimpleResource</span></span>](./Select-AzureStorSimpleResource.md)


