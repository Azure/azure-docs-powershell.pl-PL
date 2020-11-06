---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: D79080D5-2785-4C46-86FD-FDAA11117D17
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: c387ebb089ab7f9dfddaee818f26596f34ed91e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552931"
---
# <span data-ttu-id="3aa72-101">Get-AzureRmDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="3aa72-101">Get-AzureRmDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="3aa72-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3aa72-102">SYNOPSIS</span></span>
<span data-ttu-id="3aa72-103">Pobiera określonego zaufanego dostawcę tożsamości w określonej usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3aa72-103">Gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="3aa72-104">Jeśli nie podano dostawcy, wyświetla listę wszystkich dostawców dla tego konta.</span><span class="sxs-lookup"><span data-stu-id="3aa72-104">If no provider is specified, then lists all providers for the account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3aa72-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3aa72-105">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3aa72-106">Opis</span><span class="sxs-lookup"><span data-stu-id="3aa72-106">DESCRIPTION</span></span>
<span data-ttu-id="3aa72-107">Polecenie cmdlet **Get-AzureRmDataLakeStoreTrustedIdProvider** pobiera określonego zaufanego dostawcę tożsamości w określonej usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3aa72-107">The **Get-AzureRmDataLakeStoreTrustedIdProvider** cmdlet gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="3aa72-108">Jeśli nie podano dostawcy, wyświetla listę wszystkich dostawców dla tego konta.</span><span class="sxs-lookup"><span data-stu-id="3aa72-108">If no provider is specified, then lists all providers for the account.</span></span>

## <span data-ttu-id="3aa72-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3aa72-109">EXAMPLES</span></span>

### <span data-ttu-id="3aa72-110">Przykład 1: uzyskiwanie określonego zaufanego dostawcy tożsamości</span><span class="sxs-lookup"><span data-stu-id="3aa72-110">Example 1: Get a specific trusted identity provider</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="3aa72-111">Zwraca dostawcę o nazwie "Moja" z konta "ContosoADL".</span><span class="sxs-lookup"><span data-stu-id="3aa72-111">Returns the provider named "MyProvider" from account "ContosoADL"</span></span>

### <span data-ttu-id="3aa72-112">Przykład 2: Wyświetlanie listy wszystkich dostawców na koncie</span><span class="sxs-lookup"><span data-stu-id="3aa72-112">Example 2: List all providers in an account</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL"
```

<span data-ttu-id="3aa72-113">Wyświetla listę wszystkich dostawców pod kontem "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="3aa72-113">Lists all providers under the account "ContosoADL"</span></span>

## <span data-ttu-id="3aa72-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3aa72-114">PARAMETERS</span></span>

### <span data-ttu-id="3aa72-115">— Konto</span><span class="sxs-lookup"><span data-stu-id="3aa72-115">-Account</span></span>
<span data-ttu-id="3aa72-116">Konto usługi Data Lake Store do pobrania zaufanego dostawcy tożsamości z</span><span class="sxs-lookup"><span data-stu-id="3aa72-116">The Data Lake Store account to retrieve the trusted identity provider from</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3aa72-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3aa72-117">-DefaultProfile</span></span>
<span data-ttu-id="3aa72-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="3aa72-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3aa72-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3aa72-119">-Name</span></span>
<span data-ttu-id="3aa72-120">Nazwa dostawcy zaufanej tożsamości do pobrania</span><span class="sxs-lookup"><span data-stu-id="3aa72-120">The name of the trusted identity provider to retrieve</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3aa72-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3aa72-121">-ResourceGroupName</span></span>
<span data-ttu-id="3aa72-122">Nazwa grupy zasobów, pod którą ma zostać pobrane określone konto zaufanego dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="3aa72-122">Name of resource group under which want to retrieve the specified account's specified trusted identity provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3aa72-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3aa72-123">CommonParameters</span></span>
<span data-ttu-id="3aa72-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3aa72-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3aa72-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3aa72-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3aa72-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3aa72-126">INPUTS</span></span>

### <span data-ttu-id="3aa72-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="3aa72-127">None</span></span>
<span data-ttu-id="3aa72-128">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="3aa72-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3aa72-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3aa72-129">OUTPUTS</span></span>

### <span data-ttu-id="3aa72-130">DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="3aa72-130">DataLakeStoreTrustedIdProvider</span></span>
<span data-ttu-id="3aa72-131">Szczegóły określonego dostawcy zaufanej tożsamości.</span><span class="sxs-lookup"><span data-stu-id="3aa72-131">The details of the specified trusted identity provider.</span></span>

### <span data-ttu-id="3aa72-132">IList<DataLakeStoreTrustedIdProvider></span><span class="sxs-lookup"><span data-stu-id="3aa72-132">IList<DataLakeStoreTrustedIdProvider></span></span>
<span data-ttu-id="3aa72-133">Lista zaufanych dostawców tożsamości na określonym koncie.</span><span class="sxs-lookup"><span data-stu-id="3aa72-133">The list of trusted identity providers in the specified account.</span></span>

## <span data-ttu-id="3aa72-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3aa72-134">NOTES</span></span>

## <span data-ttu-id="3aa72-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3aa72-135">RELATED LINKS</span></span>

