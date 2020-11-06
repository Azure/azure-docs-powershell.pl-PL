---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: FDD2CE98-6C7E-4B95-BA5B-B03B6AC6EAEF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/New-AzureRmStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/New-AzureRmStorageAccountKey.md
ms.openlocfilehash: 76b7ea9eb4a248071025ef359d6bf0877b35fe89
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554176"
---
# <span data-ttu-id="ca34f-101">New-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="ca34f-101">New-AzureRmStorageAccountKey</span></span>

## <span data-ttu-id="ca34f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ca34f-102">SYNOPSIS</span></span>
<span data-ttu-id="ca34f-103">Generuje ponownie klucz magazynu dla konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="ca34f-103">Regenerates a storage key for an Azure Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca34f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ca34f-104">SYNTAX</span></span>

```
New-AzureRmStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca34f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ca34f-105">DESCRIPTION</span></span>
<span data-ttu-id="ca34f-106">Polecenie cmdlet **New-AzureRmStorageAccountKey** generuje klucz magazynu dla konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="ca34f-106">The **New-AzureRmStorageAccountKey** cmdlet regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="ca34f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ca34f-107">EXAMPLES</span></span>

### <span data-ttu-id="ca34f-108">Przykład 1. Regeneruj klucz magazynu</span><span class="sxs-lookup"><span data-stu-id="ca34f-108">Example 1: Regenerate a storage key</span></span>
```
PS C:\>New-AzureRmStorageAccountKey -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -KeyName "key1"
```

<span data-ttu-id="ca34f-109">To polecenie generuje klucz magazynu dla określonego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="ca34f-109">This command regenerates a storage key for the specified Storage account.</span></span>

## <span data-ttu-id="ca34f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ca34f-110">PARAMETERS</span></span>

### <span data-ttu-id="ca34f-111">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="ca34f-111">-KeyName</span></span>
<span data-ttu-id="ca34f-112">Określa klucz, który należy wygenerować.</span><span class="sxs-lookup"><span data-stu-id="ca34f-112">Specifies which key to regenerate.</span></span>
<span data-ttu-id="ca34f-113">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="ca34f-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ca34f-114">key1</span><span class="sxs-lookup"><span data-stu-id="ca34f-114">key1</span></span> 
- <span data-ttu-id="ca34f-115">key2</span><span class="sxs-lookup"><span data-stu-id="ca34f-115">key2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: key1, key2

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca34f-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ca34f-116">-Name</span></span>
<span data-ttu-id="ca34f-117">Określa nazwę konta magazynu, dla którego ma zostać ponownie wygenerowany klucz magazynu.</span><span class="sxs-lookup"><span data-stu-id="ca34f-117">Specifies the name of the Storage account for which to regenerate a storage key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca34f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca34f-118">-ResourceGroupName</span></span>
<span data-ttu-id="ca34f-119">Określa nazwę grupy zasobów zawierającej konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="ca34f-119">Specifies the name of the resource group that contains the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca34f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca34f-120">-DefaultProfile</span></span>
<span data-ttu-id="ca34f-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ca34f-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca34f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca34f-122">CommonParameters</span></span>
<span data-ttu-id="ca34f-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca34f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca34f-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca34f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca34f-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ca34f-125">INPUTS</span></span>

## <span data-ttu-id="ca34f-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ca34f-126">OUTPUTS</span></span>

## <span data-ttu-id="ca34f-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ca34f-127">NOTES</span></span>

## <span data-ttu-id="ca34f-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ca34f-128">RELATED LINKS</span></span>

[<span data-ttu-id="ca34f-129">Get-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="ca34f-129">Get-AzureRmStorageAccountKey</span></span>](./Get-AzureRmStorageAccountKey.md)


