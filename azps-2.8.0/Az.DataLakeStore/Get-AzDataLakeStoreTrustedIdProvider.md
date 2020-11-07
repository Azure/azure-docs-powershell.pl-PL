---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D79080D5-2785-4C46-86FD-FDAA11117D17
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: d075c6792134536be84643d51f37b2379b63d5e8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705808"
---
# <span data-ttu-id="39da9-101">Get-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="39da9-101">Get-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="39da9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="39da9-102">SYNOPSIS</span></span>
<span data-ttu-id="39da9-103">Pobiera określonego zaufanego dostawcę tożsamości w określonej usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="39da9-103">Gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="39da9-104">Jeśli nie podano dostawcy, wyświetla listę wszystkich dostawców dla tego konta.</span><span class="sxs-lookup"><span data-stu-id="39da9-104">If no provider is specified, then lists all providers for the account.</span></span>

## <span data-ttu-id="39da9-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="39da9-105">SYNTAX</span></span>

```
Get-AzDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39da9-106">Opis</span><span class="sxs-lookup"><span data-stu-id="39da9-106">DESCRIPTION</span></span>
<span data-ttu-id="39da9-107">Polecenie cmdlet **Get-AzDataLakeStoreTrustedIdProvider** pobiera określonego zaufanego dostawcę tożsamości w określonej usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="39da9-107">The **Get-AzDataLakeStoreTrustedIdProvider** cmdlet gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="39da9-108">Jeśli nie podano dostawcy, wyświetla listę wszystkich dostawców dla tego konta.</span><span class="sxs-lookup"><span data-stu-id="39da9-108">If no provider is specified, then lists all providers for the account.</span></span>

## <span data-ttu-id="39da9-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="39da9-109">EXAMPLES</span></span>

### <span data-ttu-id="39da9-110">Przykład 1: uzyskiwanie określonego zaufanego dostawcy tożsamości</span><span class="sxs-lookup"><span data-stu-id="39da9-110">Example 1: Get a specific trusted identity provider</span></span>
```
PS C:\> Get-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="39da9-111">Zwraca dostawcę o nazwie "Moja" z konta "ContosoADL".</span><span class="sxs-lookup"><span data-stu-id="39da9-111">Returns the provider named "MyProvider" from account "ContosoADL"</span></span>

### <span data-ttu-id="39da9-112">Przykład 2: Wyświetlanie listy wszystkich dostawców na koncie</span><span class="sxs-lookup"><span data-stu-id="39da9-112">Example 2: List all providers in an account</span></span>
```
PS C:\> Get-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL"
```

<span data-ttu-id="39da9-113">Wyświetla listę wszystkich dostawców pod kontem "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="39da9-113">Lists all providers under the account "ContosoADL"</span></span>

## <span data-ttu-id="39da9-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="39da9-114">PARAMETERS</span></span>

### <span data-ttu-id="39da9-115">— Konto</span><span class="sxs-lookup"><span data-stu-id="39da9-115">-Account</span></span>
<span data-ttu-id="39da9-116">Konto usługi Data Lake Store do pobrania zaufanego dostawcy tożsamości z</span><span class="sxs-lookup"><span data-stu-id="39da9-116">The Data Lake Store account to retrieve the trusted identity provider from</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39da9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39da9-117">-DefaultProfile</span></span>
<span data-ttu-id="39da9-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="39da9-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="39da9-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="39da9-119">-Name</span></span>
<span data-ttu-id="39da9-120">Nazwa dostawcy zaufanej tożsamości do pobrania</span><span class="sxs-lookup"><span data-stu-id="39da9-120">The name of the trusted identity provider to retrieve</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39da9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39da9-121">-ResourceGroupName</span></span>
<span data-ttu-id="39da9-122">Nazwa grupy zasobów, pod którą ma zostać pobrane określone konto zaufanego dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="39da9-122">Name of resource group under which want to retrieve the specified account's specified trusted identity provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39da9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39da9-123">CommonParameters</span></span>
<span data-ttu-id="39da9-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39da9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39da9-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39da9-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39da9-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="39da9-126">INPUTS</span></span>

### <span data-ttu-id="39da9-127">System. String</span><span class="sxs-lookup"><span data-stu-id="39da9-127">System.String</span></span>

## <span data-ttu-id="39da9-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="39da9-128">OUTPUTS</span></span>

### <span data-ttu-id="39da9-129">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="39da9-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="39da9-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="39da9-130">NOTES</span></span>

## <span data-ttu-id="39da9-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="39da9-131">RELATED LINKS</span></span>