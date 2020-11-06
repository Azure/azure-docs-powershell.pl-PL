---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRMVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRMVMSqlServerExtension.md
ms.openlocfilehash: 19d4022fcf5f3eee0ee8d77e7c061ae2f8d00629
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553356"
---
# <span data-ttu-id="2482d-101">Remove-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="2482d-101">Remove-AzureRmVMSqlServerExtension</span></span>

## <span data-ttu-id="2482d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2482d-102">SYNOPSIS</span></span>
<span data-ttu-id="2482d-103">Usuwa rozszerzenie programu SQL Server z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2482d-103">Removes a SQL Server extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2482d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2482d-104">SYNTAX</span></span>

```
Remove-AzureRmVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2482d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2482d-105">DESCRIPTION</span></span>
<span data-ttu-id="2482d-106">Polecenie cmdlet **Remove-AzureRmVMSqlServerExtension** usuwa rozszerzenie serwera AzureSQL z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2482d-106">The **Remove-AzureRmVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="2482d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2482d-107">EXAMPLES</span></span>

### <span data-ttu-id="2482d-108">Przykład 1: Usuwanie rozszerzenia programu SQL Server</span><span class="sxs-lookup"><span data-stu-id="2482d-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzureRMVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="2482d-109">To polecenie usuwa rozszerzenie programu SQL Server z maszyny wirtualnej o nazwie ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="2482d-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="2482d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2482d-110">PARAMETERS</span></span>

### <span data-ttu-id="2482d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2482d-111">-DefaultProfile</span></span>
<span data-ttu-id="2482d-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2482d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2482d-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2482d-113">-Name</span></span>
<span data-ttu-id="2482d-114">Określa nazwę rozszerzenia programu SQL Server, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2482d-114">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2482d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2482d-115">-ResourceGroupName</span></span>
<span data-ttu-id="2482d-116">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2482d-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="2482d-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="2482d-117">-VMName</span></span>
<span data-ttu-id="2482d-118">Określa nazwę maszyny wirtualnej, z której to polecenie cmdlet usuwa rozszerzenie programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="2482d-118">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2482d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2482d-119">CommonParameters</span></span>
<span data-ttu-id="2482d-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2482d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2482d-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2482d-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2482d-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2482d-122">INPUTS</span></span>

## <span data-ttu-id="2482d-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2482d-123">OUTPUTS</span></span>

## <span data-ttu-id="2482d-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2482d-124">NOTES</span></span>

## <span data-ttu-id="2482d-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2482d-125">RELATED LINKS</span></span>

[<span data-ttu-id="2482d-126">Get-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="2482d-126">Get-AzureRmVMSqlServerExtension</span></span>](./Get-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="2482d-127">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="2482d-127">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)


